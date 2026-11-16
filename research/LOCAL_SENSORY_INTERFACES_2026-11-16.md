# Local audio, lightweight vision, touch and safe integration
**Public desk research: 2026-11-16** · This document describes candidate interfaces and research tests, **not** tested hardware or certified robot behavior.

## Priority and safety architecture

| Layer | Research priority | Capability | What is still unproven |
|---|---|---|---|
| **Audio** | 1 — first prototype | Local wake / voice activity / speech recognition / synthesized reply / interruption | Real machine latency in noise, false alarms, input-output permissions and cloud independence of any language-model call |
| **Lightweight vision** | 2 — stationary perception first | Camera stream, basic presence/object detection, potential local face-free scene observation | Depth, clearance, safe stopping distance, stairs/thresholds, moving-platform reliability |
| **Tactile/force** | 3 — after robot choice | Existing touch sensors or force/torque telemetry, where manufacturer allows local access | Safe hugs, skin/covering modifications, reproducible force calibration, warranty and sensory permissions |

**Fundamental constraint:** a computer-hosted speech/vision application, a cloud agent, or a large language model must **never be the sole emergency-stop, fall-prevention, motor-current or collision safety path**. Local motor control, physical stop and independent deterministic safety supervision belong on the approved machine controller. ROS2 navigation collision monitors are useful but are not themselves certified functional safety systems: https://docs.nav2.org/jazzy/configuration_and_development/configuration_guide/core_servers/collision_monitor/configuring_collision_monitor_node/

## 1. Local-first audio options
| Step | Public software reference | Caveat |
|---|---|---|
| Wake word | **openWakeWord**, local ~16 kHz audio input and short inference frames: https://github.com/dscripka/openWakeWord | false positives with TV, accents and background speech; license/model and language support |
| Voice activity / interruption | **Silero VAD**, CPU-capable 8kHz/16kHz VAD: https://github.com/snakers4/silero-vad | VAD detects speech, not words; output cancellation and echo suppression must be integrated |
| Speech-to-text | **whisper.cpp**, local C/C++ inference with Windows/CPU paths and a demo stream: https://github.com/ggml-org/whisper.cpp | demo ≠ measured low-latency production recognition on a particular PC |
| Text-to-speech | **Piper**, maintained under Open Home Foundation: https://github.com/OHF-Voice/piper1-gpl | verify engine GPL requirements and each individual voice model's license |
| Answering | Locally running or externally hosted language model through an intentionally bounded interface | Offline STT/TTS does **not** imply an API-hosted LLM is offline; decide explicitly whether any text leaves the machine |

**No-purchase bench proposal** (not executed): in a normal non-sensitive workspace, test `wake -> VAD -> STT -> generate/return text -> TTS` using synthetic or licensed test audio and consenting users. Support barge-in (speaker output cancelled on new speech), mute, privacy-by-default, local timeout. Log **durations, CPU/RAM and error rates**, not raw audio. Record median/p95 speech-to-first-audio delay, false wakes, cancellations, speaker/microphone echo and noise effects. Published software existence is **not evidence of successful local deployment**.

## 2. Light vision, limited to non-safety development
- A standard locally connected USB camera can capture basic RGB images; **640×480 at 10–15 fps** is merely a possible *starting benchmark*, not a mandatory robotics specification or verified performance figure.
- Example locally processable detector: **Google MediaPipe Object Detector** (image/video/live-stream modes), https://developers.google.com/edge/mediapipe/solutions/vision/object_detector . Busy asynchronous processing may drop frames.
- RGB object boxes do not provide reliable collision geometry, door width/clearance, stair edges, ground profile, seat depth or stop distance. Before real mobile autonomy, identify and calibrate suitable **depth, stereo, ToF, LiDAR, tactile/encoders or other range sensing** with the platform manufacturer.
- Stationary webcam classification can be prototyped off-board without buying a GPU, but every camera has data governance and retention requirements. Verify camera permissions and any mandatory internet access.
- Human presence recognition is not permission to collect identity/face data; avoid unnecessary personal biometric processing or recording.

## 3. Manufacturer I/O and edition dependencies
**A documented local interface is a partial fact, not a whole-life cloud independence guarantee.**

| Robot/platform | Audio/public I/O | Vision/public I/O | Contact/touch | Access status & key unanswered permission |
|---|---|---|---|---|
| **Fourier GR-3** | OEM head developer documentation covers mic/speakers, some echo processing | Local head camera API (Android head module) | OEM describes distributed sensors; optional **FDH-12** hand tactile topic via DDS, not necessarily every hand model | FourierDDS C++/Python integration exists; verify purchased edition, raw stream access, WAN-independent restore and impact on warranty |
| **AGIBOT X2** | OEM microphone/speaker/screen product claims | Plain **X2** RGB camera; **X2 Ultra** additionally lists RGB-D and 3D LiDAR — **do not assume Ultra sensors at base price** | OEM simple head touch, not proof of tactile hands | Raw sensor APIs, local access license, firmware recovery and third-party accessory permissions **UNKNOWN** |
| **Fauna Sprout** | Mic array, speakers | OEM ZED 2i stereo camera, ToF, onboard Jetson | Soft covering does **not** establish accessible force sensors | Local programming claim; UK delivery and recovery/data rights **UNKNOWN** |
| **NEURA 4NE1** | Local NEURON AI marketed | Local 3D vision marketed | Sensorized skin/touch & proprioception marketed | Verify model-specific SDK access and privacy; Neuraverse ecosystem and local compute are distinct |
| **1X NEO** | Speech advertised; third-party raw mic/speaker SDK **UNKNOWN** | Cameras and remote Expert Mode public; third-party raw stream rights **UNKNOWN** | Tendon drive and fabric do not constitute independent contact-safety certification | Third-party local SDK, permanent remote disable, offline support and UK warranty **UNKNOWN** |
| **Pollen Reachy 2** *(interface reference, wheeled)* | Local SDK audio examples | Local SDK camera/depth examples | Application-specific | Strong local API reference, but wheeled morphology does not meet an ordinary biped chair requirement |

**OEM source links:**
- Fourier general: https://support.fftai.com/en/gr3/getting-started/general-information ; head: https://support.fftai.com/en/gr3/development/head-domain-development ; hand: https://support.fftai.com/en/gr3/modules/gr-endeffector ; DDS: https://support.fftai.com/en/gr3/modules/fourierdds
- AGIBOT X2 SKU differences: https://www.agibot.com/products/X2
- Fauna Sprout: https://faunarobotics.com/product
- NEURA NEURON AI and 4NE1: https://neura-robotics.com/neuron-ai/ ; https://neura-robotics.com/products/4ne1/
- 1X NEO: https://www.1x.tech/order
- Pollen SDK video: https://docs.pollen-robotics.com/developing-with-reachy-2/basics/8-get-images-from-cameras/ ; audio: https://docs.pollen-robotics.com/developing-with-reachy-2/basics/9-play-record-sound/

## 4. Generic local integration design, without private computer details
- **High-level agent**: manages dialogue and abstract intents; runs on a separate computer if desired, but no raw physical actuator authority.
- **Bounded local interface**: authenticated, least-privilege command channel; high-level request such as `speak(text)` or `request_safe_posture()`; status/telemetry in a separate return channel, with explicit timeouts. Ethernet or segmented Wi-Fi possible **if OEM allows**. Do not share private memory storage with a vendor service process.
- **Robot controller**: executes only commands within documented safe limits; validates state, obstacle and stop signals locally. Unexpected message loss must result in a well-defined safe state, not unbounded movement/retry.
- **Independent stop**: physical E-stop and approved fail-safe hardware remain functional when the agent computer, network or cloud disappears.
- **Warranty/data rule**: externally attaching speakers, cameras, force sensors or altering clothing can interfere with sensor fields-of-view, cooling or joint dynamics. Written OEM approval is needed to know which changes preserve warranty.

## Unanswered supplier questions (no outreach authorization implied)
1. Can an owner obtain *raw mic/speaker and RGB/depth timestamped streams locally*, with WAN disconnected and no compulsory manufacturer cloud speech service?
2. Which camera/depth/touch capabilities are **standard on this exact SKU** and which paid options?
3. Can an authorized external computer publish bounded high-level goals and observe status without access to proprietary low-level motor controls?
4. Does third-party attachment affect safety certification, regulatory intended use, license, security patches and warranty?
5. Does manufacturer support **local-only initial setup, recovery and diagnosis** with private storage physically separated during servicing?

**Bottom line:** begin with software-only voice interaction and stationary non-safety visual research; do not buy new compute or sensors solely because a manufacturer product page mentions ROS2/DDS/Jetson. Real home mobility requires an independently engineered safety case and platform-specific permission evidence.
