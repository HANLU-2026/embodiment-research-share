# Humanoid power, UK household charging, and offline software lifecycle | Four-candidate evidence review
**Date:** 2026-11-16 | **Status:** Corrected editorial consolidation of Gemini's 2026-11-16 research draft, reviewed against public OEM pages and UK/IATA transport guidance. **No hardware testing, OEM written confirmation, insurance quote, or procurement.**

**Scope:** AGIBOT X2 Neo / X2 Ultra New Version (different SKUs), NEURA 4NE1 Gen4, Fourier GR-3, 1X NEO. Do **not** import specs from older models or other Fourier product families.

Related:
- [UK shortlist](UK_HUMANOID_CANDIDATES_2026-11-16.md)
- [Sit/rise, floors and local audio](HUMANOID_POSTURE_HOME_AUDIO_FOLLOWUP_2026-11-16.md)
- [Physical E-stop, one-person rescue and UK home insurance](HUMANOID_ESTOP_RECOVERY_UK_INSURANCE_2026-11-16.md)
- [Local sensor and interface separation](LOCAL_SENSORY_INTERFACES_2026-11-16.md)

## Verdict
**All remain WATCH; household procurement frozen.** Power capacity and local SDK presence do not establish safe power-loss posture, UK plug/approval, autonomous safe charging, long-term offline activation or emergency rescue. Never downgrade the August 2027 safety objective merely because a public spec is attractive.

**Evidence legend:** A = explicit OEM technical/store text *for a named SKU* (not independently tested); B = broader OEM promotion or uncertain SKU scope; C = independent third-party reported information; U = not established in this public review. Mark factual subclaims separately; unknown ≠ unsupported.

## 1. UK home electricity / battery evidence

| Candidate | OEM-published battery / endurance | AC input and UK compatibility | Safe loss-of-power state | Evidence / caution |
|---|---|---|---|---|
| **AGIBOT X2 Neo** | **~500Wh**, about **2h walking at 0.5 m/s**, **≤1.5h charging**, **swappable battery** **[A: current X2 Neo store]**. Does not prove live hot swap or owner-safe battery handling. | Store lists **“Input Voltage 100~220V” [A: page text]**, but does **not** prove supplied charger is rated for **230V/50Hz UK mains**; ask for charger nameplate, 230V tolerance, UK plug, conformity documentation **[U]**. | Battery-low controlled posture, complete energy failure/joint brake, and safe solo recovery **[U]**. | **Secondary development NOT supported [A]**; do not use AimDK development or X2 Ultra RJ45 capabilities as Neo rights. |
| **AGIBOT X2 Ultra New Version** | Same OEM store general values **~500Wh**, **~2h**, **≤1.5h**, replaceable **[A]**, ~39kg **[A]**. No validated home-duty cycle. | Same published “100~220V” listing; suitability for UK 230V *not yet established* **[U]**. | Battery-depletion and unexpected power loss **[U]**; earlier AimDK X2/X2 Ultra seated shutdown and emergency procedures are not automatically valid for New Version. | **Secondary development supported [A]**; **RJ45 x2, Orin NX** specified, but permission to use raw built-in mic/speaker and permanent air-gap operation **[U]**. |
| **NEURA 4NE1 Gen4** | Gen4-specific Wh, charge duration, user replaceability, idle/active duty cycle **[U]**. Do not transfer Gen3.5 specs. | Gen4 charger model/plate, UK lead/plug, clearances and electrical declaration **[U]**. Country of manufacturer is not proof of charger specification. | Loss of voltage/E-stop joints and 1-person recovery **[U]**. | Official page discusses 80kg in a model-family performance area while also saying Gen4 is 20% lighter than predecessor; **do not label 80kg a confirmed Gen4-only weight without SKU-specific datasheet [U for Gen4 attribution]**. |
| **Fourier GR-3** | **702Wh + 234Wh**, **~3h runtime**, **~1.5h recharge**, **hot-swappable battery** **[A: official GR-3 overview]**. | **90–260V AC, 50/60Hz adaptor input [A]** directly covers **UK 230V/50Hz**. Actual UK-supplied plug, fuse, conformity docs and installation requirements **[U]**. | Complete power loss, depleted battery, independent braking and disabled-body extraction **[U]**. Physical E-stop may cut motor power and lead to unsupported posture per OEM teleoperation SOP; see E-stop report. | **71kg [A]**; official setup/shutdown documents require hoist/transfer machine in stated procedures. Battery hot swap ≠ safe operation without protected shutdown. |
| **1X NEO** | **842Wh**, **4h claimed runtime**, **6 min charge per 1h runtime**, **self-charging** **[A: official product page claims, NOT field test]**. | US launch information; exact UK 230V/50Hz charger, UK plug and UK delivery eligibility **[U]**. | Low-charge landing / sudden shutdown mechanical outcome **[U]**. | **~30kg [A]**, 22dB is an OEM nominal advertised noise level, not an independently tested home/nighttime figure. Owner-replaceable battery **[U]**, not proven “non-replaceable”. |

### Sources by platform
- AGIBOT current SKU comparison: https://store.agibot.com/products/x2 and https://store.agibot.com/products/x2-ultra . **Read both versions; the old AimDK manual does not establish New Version features.**
- AGIBOT series public FAQ: https://store.agibot.com/collections/humanoid-robot . This page says **8 months' maintenance service (X2) versus 18 months' maintenance service (Ultra)**; **do NOT relabel this a verified whole-machine warranty**. Exact Neo and Ultra New Version warranty duration and geographical applicability need purchase terms.
- Fourier GR-3 manufacturer specifications: https://support.fftai.com/en/gr3/getting-started/general-information
- NEURA official Gen4/product family: https://neura-robotics.com/products/4ne1/ ; Gen4 announcement 2026-10-22: https://neura-robotics.com/tum-robogym-munich-4ne1-gen4-launch/
- 1X official product and conditions: https://www.1x.tech/neo ; https://www.1x.tech/order

## 2. Software update and permanent offline control matrix

| Model | Publicly established | **NOT** established (the actual purchase gate) |
|---|---|---|
| **X2 Neo** | OTA/App/remote controller are marketed [A]; **secondary development not supported [A]** | First-boot without OEM account; raw mic/speaker access; permanent local high-level API; offline firmware recovery/rollback; refusal of OTA without disablement; independent computer/WAN-block warranty [U]. |
| **X2 Ultra New Version** | OEM says secondary development supported; local RJ45 and compute present [A]. Older AimDK manuals demonstrate partial local control for earlier versions [B relative to this SKU]. | Exact new-version ROS/DDS/OS/firmware licence, air-gapped first boot, raw audio, signed offline recovery, non-expiring local activation and UK warranty of third-party compute [U]. |
| **NEURA Gen4** | OEM says NEURON AI perception/action runs locally on robot and Neuraverse connects skills and ecosystem [B]. | “Local AI” is not a written guarantee of account-free boot, offline skills, lifetime licensing, USB/air-gapped service repair, offline audio API or safe stop upon loss of WAN [U]. |
| **Fourier GR-3** | OEM technical pages identify Ubuntu 22.04, Ethernet, local developer APIs/FourierDDS [A]. | Local application development is **not** proof that motor controller firmware, licence activation, official speech stack, factory recovery and warranty work offline indefinitely [U]. |
| **1X NEO** | OEM offers autonomous baseline, scheduled Expert Mode, app-based monitoring/control and OTA-progressive skills [B/A for feature advertising]; $20k ownership vs $499/month subscription tiers [A]. | Air-gapped initial activation, local raw mic/audio/movement interface, whether owner may permanently disable Expert Mode and telemetry without losing warranty, whole-life base functionality with no OTA, offline restore and UK support [U]. **Do not claim its Redwood AI is fully offline solely from onboard compute.** Do not assume the exact consequences of subscription expiry without contract text. |

**Non-negotiable separation:** an owner-owned ThinkPad can implement wake/VAD/STT/TTS offline; that does *not* imply access to the robot's embedded microphones/speakers or turn a vendor-cloud-controlled robot into a sovereign device. Physical E-stop, balance, braking, fall protection and battery safeguards must run on an OEM-approved machine-local safety architecture independently of ThinkPad, Wi-Fi, voice app or LLM.

## 3. Lithium battery transport into Britain — do not apply one rule to every shipment

- All four advertised batteries are **well above 100Wh**, but the relevant legal transport code depends on **battery shipped by itself**, **battery packed alongside equipment** or **battery contained in equipment**, and **road/rail, sea, or air**. Do not declare every battery shipment UN3480 or categorically require the battery to be physically removed from a robot. Obtain a shipper-specific classification.
- **Air freight:** IATA's **2026** guidance requires **≤30% state of charge** for lithium-ion batteries **packed with equipment** (PI 966; subject to limited approval exceptions); for batteries **contained in equipment** (PI 967), ≤30% is **strongly recommended, not universally mandatory**. A statement that all international robot shipments “must have 30% charge” is inaccurate. See IATA: https://www.iata.org/en/programs/cargo/dangerous-goods/lithium-batteries/ and guidance document https://www.iata.org/contentassets/05e6d8742b0047259bf3a700bc9d42b9/lithium-battery-guidance-document.pdf
- UK aviation regulator requires compliant battery testing, marking/packing/docs and competent dangerous-goods transport; **UN 38.3 test summary**, appropriate dangerous-goods declaration where applicable, and OEM/forwarder assignment of responsibilities. https://www.caa.co.uk/safety-initiatives/safety-projects/transport-of-lithium-batteries/
- **UK government separates air (IATA/ICAO), road (ADR), and sea (IMDG)**. Cross-border EU/UK shipment may be road/ferry, not an “aircraft hand luggage 100/160Wh” question. https://www.gov.uk/moving-dangerous-goods/rules-for-different-types-of-transport
- Ask for the **exact SKU's battery UN38.3 test summary, SDS where provided, shipment classification, packed/installed configuration, applicable transport mode and seller/forwarder liability**, before quoting a UK landed cost or return logistics.

## 4. Decision gates and targeted written questions

**P0 / block domestic purchase pending proof:**
1. **Emergency & failure posture.** For low-charge auto shutdown, *instant battery disconnect*, physical E-stop, communication loss, and a stationary robot on a 42–46cm chair, provide distinct states for torque/brake/controlled descent and an OEM-approved **one-adult** removal procedure. See E-stop memo.
2. **Never-bricked local ownership.** For exact SKU, written matrix of offline initial activation, indefinite basic walk/stand/sit and audio use, local API authorization, OTA refusal, factory reset, firmware rollback, vendor server retirement, account suspension, purchased vs subscribed licence.
3. **Owner AI and privacy.** Confirm authorized high-level PC interface, local raw mic/speaker access where needed, no raw motor command authority for LLM, permanent opt-out/disablement of OEM remote expert/cloud data access, service logs and warranty when WAN access is physically blocked.
4. **Practical UK energy & safe charging.** Exact adaptor/charger **nameplate** (input voltage/frequency, power, plug and fuse), BS1363 supply lead if applicable, UK supply conformity documents, thermal/ventilation safe clearances, supervised charging instructions, charging fire protections, emergency shutdown and battery disposal.
5. **UK battery shipping & rescue.** Confirm shipper/repairer takes responsibility for shipment classification, tested battery documentation, pickup of defective batteries, UK spare stock and single-person rescue support in an actual home.

**P1 / commercial check:** paid app/skills/licence fees, update policy/lifetime dates, access to signed offline recovery image, UK after-sales assistance and parts, exact purchase warranty (separately from maintenance service), insurance declarations and actual landed price.

### Short exact-SKU OEM request (not sent)
> For [MODEL, SKU, FIRMWARE, COUNTRY UK, PURCHASE/LICENCE VARIANT], please provide (a) exact supplied charger nameplate/UK lead and unattended charge instructions, (b) safe low-voltage/complete-power-loss/E-stop joint and fall behavior and one-adult recovery SOP, (c) first-boot and ongoing operation with WAN permanently disconnected, (d) licensed locally accessible speech and high-level movement interfaces, (e) OTA refusal, signed offline restoration/rollback and support at end-of-service, and (f) third-party computer/network-isolation warranty coverage and UK battery transport/repair provisions. Please distinguish public marketing from the supplied contract; mark unavailable evidence explicitly.

## 5. Editorial corrections to Gemini's submitted draft
1. **GR-3 UK electrical input** was marked unknown in the draft: OEM actually publishes **90–260V, 50/60Hz**; UK *plug and delivery conformity* remain unknown.
2. **AGIBOT “8-month/18-month warranty”** in draft: the store says **maintenance service duration**. Do not treat that phrase as the full legal warranty or exact Neo/New-Version sale term.
3. **Gen4 is 80kg** in draft: the official product page lists 80kg but also describes Gen4 as 20% lighter; version association of the spec block is not explicit enough to treat the **80kg as a signed Gen4 datasheet value**.
4. **NEO 842Wh / 4h / quick charge** are explicitly on the official product page: label **A as an OEM claim**, not B solely because they are marketing figures. No field performance proven.
5. **“All UK chargers unknown”** was too broad (Fourier documented), while AGIBOT current store's **100–220V input** makes a physical UK nameplate/230V query especially important.
6. **1X battery nonreplaceability, indefinite subscription lockout, fully offline Redwood, and warranty automatically void upon offline operation** are **not established** from sources reviewed; keep U / contract question.
7. **Air shipping 30% SoC and compulsory battery removal** are not universal across transport mode/configuration; use current IATA/CAA instructions and carrier's own classification.
8. **No solo adult could ever lift 71kg** is an unsafe universalization; the real requirement is the existence of a **manufacturer-approved, practicable solo-home rescue and relocation procedure**, not an anatomical guess.

## Execution / provenance
Prepared as **Gemini research synthesis, revised by Sol with original OEM/regulator evidence**. Public web review only. No supplier email sent, no OEM guarantee received, no UK insurance quotation secured, no device/charger certified by this note. Shared file is for review and follow-up, not an authorization to deploy or experiment unsafely.
