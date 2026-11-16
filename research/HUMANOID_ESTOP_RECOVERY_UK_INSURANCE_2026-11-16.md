# Four humanoid watch candidates | Emergency stop, single-person recovery and UK household insurance
**Desk review: 2026-11-16** · Scope: AGIBOT X2 (SKU must be specified), NEURA 4NE1 Gen4, Fourier GR-3, 1X NEO. **No physical test, insurance quote, warranty approval, or purchase authorization.** This is an evidence-led safety screening, not an engineering safety certification or legal opinion.

Related: [Four-platform posture and local audio follow-up](HUMANOID_POSTURE_HOME_AUDIO_FOLLOWUP_2026-11-16.md) · [UK candidate shortlist](UK_HUMANOID_CANDIDATES_2026-11-16.md) · [Local sensor/control boundaries](LOCAL_SENSORY_INTERFACES_2026-11-16.md).

## Executive decision (no change to procurement freeze)

1. **Do not purchase, reserve or downgrade the household safety gate yet.** No exact candidate SKU has shown, with written OEM evidence, a complete unassisted home emergency-stop + recovery procedure, including a single adult moving a disabled robot from a chair or narrow corridor.
2. **AGIBOT X2 AimDK:** the official non-gantry *lay-down from standing* procedure explicitly calls for **at least two operators** in the lowering phase. Seated shutdown can dispense with a gantry only when the robot is supported on a **35–40 cm** stable stool/platform and braced by a person/backrest during zero-torque entry. This is NOT a one-person fall-recovery validation and does not automatically apply to **X2 Neo**.
3. **Fourier GR-3:** official startup/shutdown instructions involve a **hoist/transfer machine**; the GR-3 teleoperation documentation says physical E-stop **cuts motor power immediately** and the robot **cannot maintain standing**. The published recovery sequence includes hoisting. It is a high-risk match for an ordinary one-adult, no-hoist UK home **under these documented operating procedures**, not proof that every possible factory configuration is identical.
4. **NEURA 4NE1 Gen4 and 1X NEO:** in this review, no exact-SKU OEM written household emergency recovery/move-without-hoist instructions were established. **UNKNOWN**, not disproved.
5. **UK insurance now has a real product lead:** Tokio Marine HCC International and Adrian Flux announced UK domestic humanoid-robot cover on **2026-10-29**. The product is attached to a household policy, not universal automatic cover. **No quotation, policy wording, coverage confirmation or acceptance of these four models was obtained.** Insurance does not mechanically prevent a fall.

## Evidence standard
- **A — OEM-direct, model/version-scoped:** an accessible manufacturer manual/technical procedure expressly describes a given behavior; not equivalent to a witnessed test or a household certification.
- **B — OEM-direct but scope limited:** public product claim, operations mode, or safety feature without an exact-SKU residential recovery test.
- **C — third-party / broker public claim:** market offering or coverage description; policy terms and individual acceptance unconfirmed.
- **U — unknown:** this review did not establish the fact. Absence of a public manual is not evidence of impossibility.
- **Safety gate PASS** requires OEM written exact-SKU confirmation plus supervised practical acceptance testing; a brochure, video or insurance page never earns PASS alone.

## A. Emergency-stop and recovery matrix

| Candidate | Manufacturer-confirmed relevant fact | Evidence | Household single-person recovery | Decision consequence |
|---|---|---|---|---|
| **AGIBOT X2 AimDK** | OEM shutdown guide: standing-preparation to ground requires at least **two operators**; controller emergency transition uses zero-torque; seated shutdown on **35–40 cm** stable support requires manual rear-handle or backrest support, with damping-first proposed as safer transition. | **A** for the covered AimDK guide only | **U** for actual fall, blocked hall, off-power 1-adult movement, independent physical hardware E-stop, **X2 Neo** correspondence | Do not treat seated mode as autonomous chair sitting or documented 1-adult disabled-body extraction. Request exact model and emergency SOP. |
| **Fourier GR-3** | Official GR-3 unpacking/open/shutdown guides require hoist; GR-3 teleoperation document: red emergency stop at rear waist, immediate motor cut, cannot remain standing; physical E-stop exit includes hoist/restart. | **A** for documented operating/teleoperation configurations | **U** for an alternative OEM-approved home mode without hoist; **no demonstrated 1-adult rescue** | **High household deployment risk** under published SOP; require an alternative written factory-approved procedure, not an improvised lift. |
| **NEURA 4NE1 Gen4** | Public product/launch material does not establish an exact-SKU single-person post-E-stop recovery method in this review. | **U** for this question | **U** | Hold. Request safety manual with exact Gen4 hardware/software revision, brake/power-loss posture, grips/lift apparatus, one-person extraction. |
| **1X NEO** | Official home-product publicity does not establish an exact-SKU E-stop mechanical state, post-fall handling and local recovery procedure in this review. | **U** for this question | **U** | Hold. Ask owner-safe rescue, physical button location, remote/Expert Mode failure interaction and UK service response. |

**Do not conflate controls.** A high-level software `stop()`, a controller mode called `zero torque`, a physical E-stop, protective stop, motor brake and safe power isolation are distinct until the OEM says otherwise. A de-energised robot may collapse; a braked robot may be too stiff/heavy for rescue. Do **not** bypass or slow an E-stop to prevent falls. Safety must remain robot-local and independent of the external ThinkPad, LLM, Wi-Fi, cloud and developer SDK.

### Specific primary records

- AGIBOT X2 AimDK, [Shutdown Guide, sections 2.4.1 and 2.4.2](https://x2-aimdk.agibot.com/en/latest/operation_guide/shutdown.html): two-operator lay-down; supported seated zero-torque shutdown. The words 'no gantry' **do not mean** independent single-person recovery.
- Fourier GR-3, [official unboxing/startup/shutdown guide](https://support.fftai.com/gr3/getting-started/operation-guidance): *开机指南（需要移位机）* and *关机指南（需移位机）*.
- Fourier GR-3, [teleoperation DAQ and data conversion, §5.2/5.4](https://support.fftai.com/en/gr3/development/teleoperation-daq-and-data-conversion): emergency power-off, inability to stand, hoist sequence, rear red E-stop. This is **teleoperation procedure evidence**, not an independently tested general consumer-use outcome.
- NEURA [4NE1 product page](https://neura-robotics.com/products/4ne1/) / [Gen4 announcement](https://neura-robotics.com/tum-robogym-munich-4ne1-gen4-launch/); 1X [NEO product/launch page](https://www.1x.tech/discover/neo-home-robot). Public product information cannot fill missing rescue manuals.

## B. UK residential insurance — established vs unproven

**Established (C / product-level, not individual policy):**
- [Tokio Marine HCC International announcement, 2026-10-29](https://www.tmhcc.com/en/news-and-articles/company-news/tokio-marine-hcc-international-and-adrian-flux-partner-to-launch-domestic-humanoid-robot-coverage): underwritten by TMHCCI; domestic humanoid cover available through Adrian Flux's UK home-insurance offering. Announced categories: robot damage/theft; sudden robot-caused home/contents damage; personal liability; emergency recovery/safe disablement after sudden malfunction.
- [Adrian Flux dedicated product page](https://www.adrianflux.co.uk/domestic-humanoid-robot-insurance/): the robot may be **specified as a possession on a home policy**; public FAQ states **up to £5,000 for sudden damage to the home or insured belongings caused by the robot**. That **£5,000 is NOT a verified blanket cap** for robot replacement or injury liability. Premium and terms are bespoke.

**NOT established (U / written broker or underwriter response required):**
1. Whether **AGIBOT X2 specific SKU, NEURA 4NE1 Gen4, Fourier GR-3 or 1X NEO** can actually be placed on this product at a given UK address and declared household use (not lab/commercial operation).
2. Eligibility when the **UK dwelling is rented**, including landlord notification/consent, building vs contents cover, pet/child presence and standard unattended operation.
3. Whether **third-party local speech/AI computer**, fully offline operation, custom firmware or attachments, independent repair, or refusing OEM telemetry/updates are accepted; disclosure duties and exclusions.
4. Full **policy wording**, personal injury/property liability limits, exclusions, deductibles, robot insured value, accidental fall vs mechanical failure, battery fire and charging incidents, optional recovery dispatch and geography/response times.
5. Whether 'emergency recovery/safe disablement' funds a contractor **who can actually access the home and lift/secure the relevant disabled model**, under what hours and cost limit. An insurance reimbursement clause does not create a physical rescue service.

### Short broker inquiry template (not sent)
> We are performing advance research for possible **2027 private residential use in Oxfordshire** of one humanoid robot. Candidate models are **AGIBOT X2 [exact SKU TBD], NEURA 4NE1 Gen4, Fourier GR-3, and 1X NEO**; **no purchase or installation is planned yet**. Does your domestic humanoid-robot policy consider each model (subject to final serial number/value), including a **rented household**? Could you share indicative eligibility requirements and the applicable policy wording/endorsement? Please identify treatment of independent on-premises AI/audio integration, air-gapped operation, OEM/third-party maintenance, unattended charging, children/pets, accidental falls, injury to visitors, and emergency lifting/recovery following physical E-stop. In particular, is an actual UK recovery contractor provided or only reimbursement, and what limits/exclusions apply? This is a research inquiry, not a bind request.

## C. Unified 12-question OEM request — exact variant and version required

Send **only with user approval / to an existing authorised supplier thread**. Ask suppliers to reply in writing; photos/uncut videos may support but not replace manuals.

1. **Exact model/SKU, firmware version, option packs and home use:** are household occupied-premises deployments an approved intended use, including children and pets nearby?
2. **Physical E-stop:** button position/number and whether a nearby adult can reach one from beside or behind the body; circuit independence from external PC, cloud, radio and application.
3. **Stop states:** for physical E-stop, protective stop, commanded stop, complete power loss and battery depletion separately, state joint torque, brake/damping behavior, balance/controlled descent and fall envelope.
4. **Standing vs sitting:** at an ordinary **42–46 cm chair** with a solid back, describe E-stop consequences, chair stability, trapped hands/feet and safe exit procedure.
5. **Single adult extraction:** can one unassisted adult (no gantry/hoist) relocate a disabled seated or fallen robot from a narrow hall/doorway? If yes, provide mass, manufacturer-approved grip points, wheels/support trolley, required clearance and step-by-step SOP.
6. **Hoist/operator requirement:** explicit minimum crew count, total load, support frame and paid onsite rescue availability in Oxfordshire; distinguish routine startup/shutdown and emergency rescue.
7. **Loss-of-comms test:** when the PC, speech agent, Wi-Fi, local API, cloud or vendor account is cut suddenly, exactly what happens to the body? Can physical E-stop still function?
8. **Contact/fall hazards:** pinch/crush zones, published impact/contact tests and allowed proximity/guarding near people and pets; do not infer safe hugs from soft skin.
9. **Recovery after fall:** steps to isolate energy, recover balance, restart safely, and check battery/joints/skin/structural integrity; precise post-fall warranty status.
10. **Video evidence:** uncut exact-SKU demonstration of supervised E-stop from moving/standing and sitting states with a protected fall environment; no unsafe live user trial requested.
11. **Local AI boundaries:** where independent voice/navigation requests enter the OEM-supported high-level interface; manufacturer confirmation that LLM agents cannot bypass safety functions.
12. **Written acceptance:** signed manual excerpt or warranty/safety support statement for UK private-home use; if unknown, expressly answer UNKNOWN and give the responsible contact.

## D. Minimum home safety gates (research policy, not certification)

- **P0 gate — cannot enter home unsupervised** without an OEM-approved, practicable fail-safe outcome (stop may involve controlled fall only with an approved separation/containment procedure) and a demonstrable recovery method available to the household.
- **P0 gate — independent stop** from any ThinkPad/LLM/API or external network. A software-only 'stop' does not suffice.
- **P0 gate — rescue practicality**: if 2 people or a hoist is mandatory, the one-adult/no-hoist criterion **fails for that procedure**, unless the household explicitly changes its operational constraints **after** risk review; no silent lowering of standards.
- **P1 gate — insurance**: disclose exact equipment and usage and obtain written coverage, limits and exclusions before paid household deployment; insurance never replaces a rescue SOP.
- **Evidence freeze**: 2027-08 is a planning milestone, not a safety waiver; all four remain **Watch / procurement hold**. Do not widen platforms for this exercise.
- **No unsupervised contact** with children/pets, no powered real-world E-stop testing without OEM-qualified safeguards and a protected test area.

## Next steps / handoff
- Sol: monitor/document OEM written emergency/recovery evidence; optionally clarify UK broker underwriting **only after outreach is authorised**; maintain this matrix.
- Gemini: separate [battery, charging, heat, UK transport] and [firmware update/rollback/offline survival] research on the same four exact SKUs. Avoid mixing with this emergency/insurance memo.
- Grok: continue independent-PC local voice research and engineering feasibility; do not use agent software as a physical safety loop.
- **No email sent, no insurer quote requested, no hardware order placed.**
