# Four watch candidates | visual evidence, sitting, UK home questions, local speech
**Public research update:** 2026-11-16 · **Scope:** ONLY AGIBOT X2, NEURA 4NE1, Fourier GR-3, 1X NEO.
**Method:** 2026-11-16 review of official OEM/UK channel product pages, operating documentation and public media. **No physical test, no supplier contract, no quotation, no procurement.** Earlier shortlist: [UK Humanoid Candidates](UK_HUMANOID_CANDIDATES_2026-11-16.md); interface baseline: [Local Sensory Interfaces](LOCAL_SENSORY_INTERFACES_2026-11-16.md).

## Executive finding — a material correction
**AGIBOT X2's official operating guide has a real `sitting startup` / `sitting shutdown` mode**, not merely a publicity photograph. However, its documented posture sequence **requires a 35–40 cm stable chair/stool, back support, and a human holding its rear handle** during key transitions. **Sitting on a chair with operator support** is not proof of **autonomous approach, ordinary adult-chair sitting, or fully autonomous rising**. Manufacturer says direct emergency zero-torque mode causes loss of joint support; OEM X2 Ultra safety guide explicitly warns emergency stop can make the robot collapse. For household use this is a critical risk. This evidence refers to X2/X2 Ultra AimDK documents, **not automatically to the currently sold X2 Neo SKU**. Sources:
- Official current [X2 startup from seated position](https://x2-aimdk.agibot.com/en/dev/operation_guide/start_up_guide.html): 35–40cm, chair with back, rear-handle assistance, controller sit-prep and stand transition.
- Official [X2 shutdown from sitting posture](https://x2-aimdk.agibot.com/en/latest/operation_guide/shutdown.html): controlled sitting, damping/zero-torque, human must support to prevent falling.
- Official [X2 Ultra V0.8.1 safety/user manual (PDF)](https://x2-aimdk.agibot.com/zh-cn/v0.8.1/_downloads/3d4e4f1753e055d54e7a7a19d6e524fb/x2_ultra_user_guide_t2.5_v0.8.1.pdf): emergency stop joint unloading and falling risk. Use HTML current operations guide for main claims if PDF rendering is unavailable.
- [X2 Neo official sales edition comparison](https://store.agibot.com/products/x2): the advertised US$25,600 X2 Neo lists **Secondary Development: Not supported** and no RJ45; X2 Ultra New Version advertises secondary development, RJ45, LiDAR/RGB-D and an **ask-for-quote** price. Edition mismatch is a hard integration risk.

## Evidence images / video / chair posture for the four watch candidates

| Platform | Official full-body images and video or media portal (click through; do not redistribute video) | Sitting / rising evidence | Confidence and limits |
|---|---|---|---|
| **AGIBOT X2** | [OEM X2 photos, demo and model table](https://www.agibot.com/products/X2); [OEM X2 instructional video index](https://www.agibot.com/filepage/278.html) (startup, voice, battery); [UK Reeco on-site/field videos](https://www.reeco.co.uk/agibot-x2) (actual UK X2 clips) | **DOCUMENTED ASSISTED SIT/STAND TRANSITIONS** for versions covered by AimDK: [startup from sitting](https://x2-aimdk.agibot.com/en/dev/operation_guide/start_up_guide.html) and [shutdown into sitting](https://x2-aimdk.agibot.com/en/latest/operation_guide/shutdown.html). Human rear-handle support and 35–40cm platform; independent no-help 42–46cm chair performance = **UNKNOWN** | HIGH official instruction evidence; **not** autonomous ordinary-chair certification. OEM page says some product illustrations are simulated and X2 Ultra only; exact Neo vs older X2 control applicability requires OEM confirmation. |
| **NEURA 4NE1 Gen 4** | [OEM full-body product/media page](https://neura-robotics.com/products/4ne1/) ; [official Gen4 launch with pictures](https://neura-robotics.com/tum-robogym-munich-4ne1-gen4-launch/) ; [OEM Gen4 media collection](https://media-neurarobotics.px.media/collections/1521010597/media) | Robot physically shown operating in TUM RoboGym, but this scan found **no verifiable, exact-model continuous autonomous ordinary-chair sit/rise footage or technical SOP**. Seated posture = **UNKNOWN**, assisted/unassisted standing from chair = **UNKNOWN**. | High confidence in announced textile-body Gen4, low in home seated actions. 2026-10-22 OEM says preparing for series production, not a UK private-home delivery agreement. |
| **Fourier GR-3** | [OEM full-body specs and product overview](https://support.fftai.com/en/gr3/getting-started/general-information); [UK RBTX image gallery and listing](https://rbtx.co.uk/en-GB/components/humanoid/fourier-gr3-humanoid-robot-care-bot); [original manufacturer demo video referenced on Fourier GR-3 owner guide](https://robodromo.com/pages/fourier-gr-3); [manufacturer companion video cited by media catalog](https://mon-robot-humanoide.fr/marques/fourier/) | **PUBLIC STATIC SOFA-SEATED PRESENTATION**: [news photo of GR-3 sitting on a sofa](https://news.mydrivers.com/1/1066/1066665.htm). This proves a *pictured posture*, not independently repeatable autonomous approach–sit–stand. Single continuous sequence, 42–46cm chair suitability, emergency rescue = **UNKNOWN**. | High evidence for external form and 71kg OEM spec; actual autonomous sit/rise unknown. Marketing claims of 'safe padded design' are **not** validated contact/fall limits. |
| **1X NEO** | [Official home product images and embedded demonstration](https://www.1x.tech/neo); [official NEO launch & product video/photography](https://www.1x.tech/discover/neo-home-robot) ; [official order page](https://www.1x.tech/order) | Home-setting promotional footage and furniture-adjacent interactions, **but no exact-version, independent verified continuous ordinary-chair autonomously sitting then standing sequence located**. Sitting/rising on 42–46cm household chair = **UNKNOWN**, not proved impossible. | OEM confirms soft 3D lattice + knit exterior, ~30kg and Expert Mode service; cloud/remote boundaries, UK service, raw local speech I/O and safe unassisted chair motion unproven. |

**Visual screening is not a physical safety grading.** Do not read soft outer skin as authorization for hugging/forceful contact or unguarded operation near children/pets. Where a manufacturer video is embedded on a webpage, cite the portal and its exact demonstration title; avoid inventing a direct media file or claiming a frame-by-frame review.

## Price: evidence vs UK landed cost
**UK landed = specific correct SKU + seller legal entity + UK supply/delivery + tax + freight/duty/customs/installation + service plan**. Without written UK offer, **UNKNOWN**, not an invented GBP conversion.

| Platform | Current cited public reference | UK landed cost |
|---|---|---|
| **AGIBOT X2 Neo** | **US$25,600**, OEM store; **not** full SDK/depth version. X2 Ultra New Version **price on request**. [Official store](https://store.agibot.com/products/x2) | **UNKNOWN** for either SKU, despite [UK Reeco integration claim](https://www.reeco.co.uk/agibot-x2). Need VAT-inclusive, exact variant quote, shipping, parts/SLA. |
| **NEURA 4NE1** | **€98,000 ex taxes and shipping**, *Gen 3.5 reservation estimate*, **NOT Gen4 price**. [OEM reservations](https://neura-robotics.com/product/4ne1-reservation/) | **UNKNOWN** (Gen4 UK price, GBP FX, seller, taxes/insurance and parts). |
| **Fourier GR-3** | **£228,787.24 excluding UK VAT and shipping**, UK RBTX public offer. [RBTX UK](https://rbtx.co.uk/en-GB/components/humanoid/fourier-gr3-humanoid-robot-care-bot) | **Base advertised UK retailer amount** £228,787.24 **plus applicable 20% VAT and freight/installation**, pending live quote, exact edition and stock. NOT a fixed all-in price. GB 20% standard VAT: https://www.gov.uk/vat-rates . |
| **1X NEO** | **US$20,000 ownership / US$499 per month** published launch terms (US deliveries first), [OEM order](https://www.1x.tech/order) | **UNKNOWN**. UK tax, transport, consumer sales, recurring cost, support/SLA and Expert Mode licensing must be verified. |

**No platform has a documented UK doorstep cost range sufficiently grounded to publish as a UK price interval.** One UK dealer's ex-VAT GR-3 listing is not a contractual final delivered quote.

## Uniform home-action & recovery vendor checklist (ask all four, exact model/software)

**Only send if/when further outreach is authorized or responding to a supplier's reply; no automatic emails from this shared document.**

1. **Door:** What is the minimum clear passage width, needed turning radius, arm clearance, self-opening door-handle capability (separate from walking through an already open door)? Include video of unedited traversal.
2. **Threshold / surface:** Maximum *tested* unassisted vertical threshold in **mm**, floor type and coefficient/traction restrictions; carpet pile, wood laminate, tiled transitions, hallway cornering, wet conditions, slopes; give model and firmware and exact failure conditions.
3. **Ordinary chair sit & rise:** On a free-standing **42–46cm seat**, no props/back-handle/gantry/human assistance, can it (a) approach, (b) align, (c) descend, (d) remain sitting, (e) stand up? Provide consecutive trials with successes/failures and uncut video. If only a 35–40cm stable stool or assisted setup is supported, say so explicitly. Explain seat stability/load and chair back contact.
4. **Emergency stop & manual extraction:** Does physical E-stop switch to power cut, zero torque, damping or joint braking? Will robot collapse and is a stand/support frame mandatory? Can *one adult without a hoist* safely move the switched-off body in a narrow UK hallway (safe grips, weight, wheels absent, spine/floor hazards)? Provide the OEM procedure and whether human presence is required.
5. **Human/pet proximity & charging:** Manufacturer-defined safe speed/force/contact envelope, hands/fingers pinch protection, battery/charger location and supervised/unattended charging conditions; domestic intended-use support and error/fall recovery.
6. **Warranty and evidence:** Are the above motions covered by supplied software and warranty? Does third-party local AI/sensors or a cosmetic cover affect warranty? Who repairs the robot in the UK? What data/log/video is demanded at failure/RMA?

Keep normal activity and E-stop distinct: a fall/limp immediate stop can be *safer than continuing motion* yet unacceptable for unsupervised close proximity. Do not solve a fall risk by disabling the emergency-stop circuit.

## Offline speech / listening: robot vs external computer must be separate

### What can be offline today (public software only)
- Local microphone → **openWakeWord** wake detection: https://github.com/dscripka/openWakeWord
- **Silero VAD** speech activity/interruption: https://github.com/snakers4/silero-vad
- **whisper.cpp** on local CPU speech recognition with downloadable model weights: https://github.com/ggml-org/whisper.cpp
- **Piper** synthesizes speech locally: https://github.com/OHF-Voice/piper1-gpl
- **Answer generation** is a distinct layer. STT/TTS can be disconnected from the Internet, **even when an external language model is not**; an external API model makes *the dialogue content flowing to the API* subject to separate privacy controls.

**All FOUR robot OEMs: complete bundled WAKE+STT+TTS guaranteed to run air-gapped with no manufacturer account or telemetry = UNKNOWN.**
There is no evidence that any of these four exposes its *built-in mic, raw audio stream, speaker or dialogue replacement rights* to arbitrary third-party code with a fully disconnected WAN. Confirm the exact model/SDK, stream permissions, audio latency, acoustic cancellation and model/voice licenses in writing. NEURA's 'local NEURON AI' does NOT necessarily mean a freely reprogrammable local Whisper/Piper pipeline; Fourier's head microphone SDK and AGIBOT's externally connected microphone instructions are partial interface evidence.

### Minimum independent-PC interface (research design, not installed)
**Physical I/O**: a working microphone, audio output and test headset/speaker; 16kHz mono PCM stream is a reasonable wake/STT capture starting format, not a guaranteed OEM robot mic spec. OS permission to access mic/speaker. Offline downloaded speech models and pinned software licenses. No extra high-performance GPU required *for a proposed initial CPU test*, but real machine speed, RAM and thermal constraints **UNTESTED**.

**Local voice loop** (data are user-owned; no household audio stored by default):
`mic -> wake detector -> VAD -> local STT -> authorized intent/text response -> local TTS -> speaker`. A barge-in event cancels ongoing speech, then returns to listening. Mute/control timeout; support noisy-room testing and p95 end-of-user-speech → start-of-audio latency. Avoid duplicate trigger from speaker echo. If the model answering is remote, explicitly indicate audio remains local but transcribed text may leave; do not falsely call whole conversation air-gapped.

**Robot link later**: only an OEM-approved local authenticated high-level interface (Ethernet preferred when supported; segmented Wi-Fi acceptable for non-safety control) with bounded `speak(text)`, `get_status()`, `request_safe_posture()`, acknowledgements and watchdog/timeout. Avoid direct raw motor commands from an agent and never assume vendor built-in audio is replaceable. If manufacturer speaker interface is closed, test with an *independent external audio endpoint* before talking about retrofits; attachment can affect warranty. Device-private memory and keys are not shared with vendor maintenance.

**Safety invariant**: physical E-stop, balance and collision/fall prevention must be robot-local and independent of off-board PC, audio application, Wi-Fi or language model. Do not use an LLM timeout as physical safety controller.

## Delta to earlier shortlist
- **X2**: upgrade evidence from generic **sitting UNKNOWN** to **ASSISTED sit/start-from-sitting and supported controlled sitting shutdown CONFIRMED in a specified operating guide**, but not autonomous domestic-chair sit–rise; downgrade confidence that entry-priced **X2 Neo** is suitable for custom local integration (its OEM store states secondary development unsupported).
- **Fourier / NEURA / NEO**: no independent exact-SKU continuous autonomous ordinary-chair sit-rise proof located; do not imply its nonexistence.
- **UK costs**: only GR-3 has a visible £-priced UK retailer reference; all final UK landed costs remain unknown.
- **Speech**: local software stack is viable *as an architecture* for independent PC. The four manufacturers' completely offline speech integration rights are not proven.
