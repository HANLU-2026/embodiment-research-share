# Four humanoid watch candidates | Residential noise, mixed floors, child/pet proximity and UK consumables
**Public desktop review: 2026-11-16** · Research only, not physical testing or independent safety approval. **Scope limited to AGIBOT X2 Neo / X2 Ultra, NEURA 4NE1 Gen4, Fourier GR-3, 1X NEO.** No new platforms, purchase, supplier outreach or insurer inquiry authorised.

Related: [UK watch shortlist](UK_HUMANOID_CANDIDATES_2026-11-16.md) · [Chair, thresholds and audio](HUMANOID_POSTURE_HOME_AUDIO_FOLLOWUP_2026-11-16.md) · [Emergency rescue/insurance](HUMANOID_ESTOP_RECOVERY_UK_INSURANCE_2026-11-16.md) · [Power, OTA and offline lifecycle](HUMANOID_POWER_FIRMWARE_LIFECYCLE_2026-11-16.md).

## Executive conclusion

**No exact candidate version has publicly established all three occupied-home gates:** (1) repeatable independently measured sound and structure-borne vibration on a UK domestic floor during real tasks, (2) repeated mixed-floor/threshold performance **without slipping, damaging flooring or causing material foot/joint wear**, and (3) validated sudden child / small-pet intrusion handling with sensor coverage, bounded approach speed and robot-local protective stop. Marketing softness, touch sensors or staged family footage never prove these. All four remain **WATCH / no deposit**.

**Important independent new finding from public OEM security documentation:** AGIBOT's [Defined Support Period](https://www.agibot.com/Defined%20Support%20Period.pdf) explicitly lists **X2 Ultra** and **X2 Neo** end-of-security-update-support date **2027-01-01** (publication offers at least 1 year and says extensions will be posted). This is a *published support-window date*, **NOT proof that products stop running or that no extension is possible**. For 2027 acquisition, ask about exact SKU, patch commitments and extended support in writing; see power/firmware addendum.

### Evidence grades
**A** = OEM written specification/manual for named product/edition; still not independently measured.
**B** = OEM promotional general claim or old/unclear edition.
**C** = independent traceable measured result identifying actual hardware, environment and method (none established here for these home-task triples).
**U** = not established by accessible documentation; not an assertion of inability. A missing value or an unloaded spec cell is U.

## 1. Four-platform evidence grid

| Robot | Noise & vibration | Floors, thresholds & wear | Child/pet coexistence | Current consequence |
|---|---|---|---|---|
| **1X NEO** | OEM product page says **“Audible noise 22dB” [A: advertised value]** and quieter than modern refrigerator. **U** for dBA weighting, microphone distance, whether idle/walking/turning/sitting, maxima, night and floor-transmitted vibration; no traceable independent multi-task home measurement established. | OEM says **washable nylon suit and shoes [A]**. **U** for shoe sole friction, laminate scratching, carpet pile, rug edges, wet tile, threshold height and long-term replacement/abrasion results. Washability is not floor protection evidence. | OEM advertises lattice/polymer soft body, covered joints and low-inertia tendon drive **[A: manufacturer claims]**; **U** for child/pet detection sensitivity, underfoot blind spots, minimum separation, stop distance, certified child/pet contact at specific speeds, and sudden small-animal crossings. | Softness and 22dB marketing are not a family-use clearance. Data/remote Expert Mode boundaries remain separate gates. |
| **AGIBOT X2 Neo / Ultra** | No exact-SKU independently measured foot-impact, actuator/fan, sit/stand or bedroom-adjacent acoustic record established **[U]**. | OEM spec says basic model has no 3D LiDAR/RGB-D vs Ultra-equipped series **[A: store/product comparison; SKU reconfirmation required]**. **U** for verified carpet/wood/tile mobility, high-pile rugs, repeated threshold wear, foot material compatibility and wear parts. | OEM product spec lists head touch and vision differences **[A]** but does **not** establish a protective-stop safety envelope for unpredictable pets/children **[U]**. No domestic child/pet approval inferred. | Ultra's sensor package is more promising for a *test plan*; sensors alone are not a certified safety function. New 2027 security patch-window question is a procurement priority. |
| **NEURA 4NE1 Gen4** | Manufacturer calls movements 'smoother' [B], not an acoustic measurement. **U** for dBA/dBC, peaks and apartment structural vibration on exact Gen4. | OEM: fabric skin, 3D perception, contact/force sensing and limb reflexes **[B: official claims]**; **U** for residential floor load/abrasion, carpet pile, thresholds, slip and wear. Gen3.5 tests must not be transferred. | 'Sensor Skin', reflex and 'safe human interaction' are manufacturer positioning **[B]**, not evidence of detection/permitted speed around *small dogs* or children, validated safeguards or safe unexpected fall **[U]**. | Await Gen4-specific manuals/datasheet and relevant domestic intended-use declaration. |
| **Fourier GR-3** | Official overview has speaker output up to **15W [A]** but **that is not walking/actuator noise**. **U** for measured acoustic/vibration levels at idle, movement and seated transitions. | Official 15° slope claim **[A: advertised]** but **max obstacle clearance height is blank [U]**. **U** for domestic carpet/wood/tile/threshold tests, floor scratching, repeated pass wear and furniture clearances. 71kg body creates a meaningful risk-assessment need, **not a known floor damage outcome**. | OEM has head/torso tactile and soft cover **[A]**; no exact-model dynamic child/pet test/stand-off/reaction timing found **[U]**. OEM **hoist-supported startup/shutdown and physical E-stop motor cut** increase occupied-home rescue burden (see prior memo). | Elevated household risk; do not infer 'care-bot' branding means home child/pet readiness. |

**Primary model sources**
- 1X NEO current specification and safety marketing: https://www.1x.tech/neo (hardware lists 22dB; washable suit/shoes and covered joints). No disclosed method for the 22dB figure on the accessed page.
- AGIBOT product comparison: https://www.agibot.com/products/X2 ; SKU-specific AimDK: https://x2-aimdk.agibot.com/zh-cn/latest/about_agibot_X2/robot_specifications.html ; user-document collection https://www.agibot.com/filepage/271.html ; security support PDF https://www.agibot.com/Defined%20Support%20Period.pdf .
- NEURA Gen4 product: https://neura-robotics.com/products/4ne1/ ; 2026 Gen4 launch: https://neura-robotics.com/tum-robogym-munich-4ne1-gen4-launch/ .
- Fourier GR-3 specs: https://support.fftai.com/en/gr3/getting-started/general-information ; operational fault FAQ: https://support.fftai.com/en/gr3/meta-information/frequently-asked-questions .

## 2. What acoustic evidence would actually be comparable?

Ask for the **identical model/firmware** and a reproducible controlled method across:
- Robot **idle/standing fan**, **walking/turning**, **42–46cm chair sitting/rising**, **charging**, and **low-battery cooling/thermal management**, recording both **LAeq** (A-weighted average) and **LAFmax** (max) with test duration, distance, room background noise and microphone geometry. Acoustic speech/music must be separately identified or disabled during motor measurement.
- Specify **floor** (timber/laminate vs tile vs carpet), robot speed, payload, gait and cooling state. Measure **structure-borne vibration** below/adjacent room where relevant; in UK terrace/flat, a 22dB airborne claim cannot predict neighbour disturbance through a floor.
- Request **unaltered recording + calibrated sound meter data** (with limitations) rather than a video whose audio compression/automatic gain control makes absolute dB invalid.
- No arbitrary quiet-hours dB pass number is claimed here. Obtain dwelling-specific nuisance/building requirements if real installation proceeds.

**Result:** 1X's **22dB is A as a manufacturer-advertised product figure, not an independent measured residential LAeq or an all-mode guarantee**. **All four still U for directly comparable occupied-home noise**.

## 3. Floor, threshold and wear protocol to require (OEM or qualified facility; NOT a user/home trial)

**Evidence matrix requested for** sealed hardwood/engineered wood, laminate, porcelain/tile including grout, **low/high-pile carpeting**, loose rugs, threshold strips (height in mm), stair edges, wet/slippery patches and mixed-surface transitions. The first three are target dry ordinary surfaces; *wet floor and unprotected stairs are hazards to evaluate or exclude, not user trials to run*.

For each exact version:
1. State permitted surface, friction/flatness/grade, **tested** sill height in mm, toe/heel contact, local ground perception, and prohibited rugs or loose objects.
2. Provide repeated-run manufacturer tests with failures/near falls, slip detection, **foot-sole scuff / abrasion**, wood/tile scratch or dent inspection, grout/threshold impact, sensor misclassification and gait derating. Report test repetitions and conditions; none assumed here.
3. Provide after-service inspection interval, foot/shoe replaceable part numbers, DIY vs OEM-only repair, UK stock, lead time and warranty effect.
4. No ad hoc stick-on pads or sole changes without OEM written approval; may alter traction, fall prevention, sensor alignment, heat and warranty.
5. A slope rating or obstacle-demo video does **not** establish safe long-term UK domestic threshold performance.

## 4. Child / small-pet proximity (P0 safety containment, NOT live trials)

**Safety rule:** Do not use a real child or animal as a test target. Start with manufacturers' written safety case, then qualified supervised tests with instrumented **surrogates/dummies** and protective barriers in an appropriate controlled area, **not an occupied home**.

Ask each OEM to distinguish:
- **Intended-use**: manufacturer approval for residential operation with children and pets *present*, and whether independently supervised vs unattended; machine min/max size/distance of objects it can detect, including *low underfoot occlusions* and sudden close crossings.
- **Dynamic response**: perception latency, minimum stop distance, emergency protective stop, maximum speed/force/kinetic energy and pinch hazards, object classification false negatives/false positives. Data from children/pet-sized surrogate tests, not staged videos.
- **Failure modes**: loss of depth sensor, camera obscuration, power cut, communications loss, network disconnect, battery depletion, fallen robot, inaccessible E-stop. Who can disable and move it safely? Safety must remain local to robot controller.
- **No physical contact assumption**: no hugging, petting, lifting, playing, following a child/pet or touching dogs until the contact load/force/fall limits are manufacturer-verified and a supervised risk assessment supports it. Soft shell and marketing claims do not prove it safe.
- **Practical household containment now**: restricted room/locked separation during movement; no unsupervised roaming with children or dogs, no access to stairs, pet feeding and sleeping corners, cables or charging areas. Local no-go-zone app maps alone cannot act as safety barriers if they have not been validated as protective safeguards.

**Relevant published safety standard:** [ISO 13482:2014](https://www.iso.org/standard/53820.html) covers personal-care service robotics, including **domestic animals and property where appropriate**. This shows why safety assessment must address pets; it does **not** certify any candidate. [ISO 13482 edition 2](https://committee.iso.org/standard/83498.html) was still **under publication** on 2026-11-16; do not claim it is already fully published or that any of the four complies.

## 5. Consumables / service lead time — add to existing UK repair due diligence

No verified UK stock/lead time, wear-rate or OEM-authorised independent repair availability established **for exact SKU** on: sole/shoe coverings, robot feet contact surfaces, tendon/cable and guides (where applicable), joint seals, cooling fan/filter, cosmetic soft skin/knit covers, tactile sensor outer layers, camera covers, charger plug/dock, battery and connectors. **Unknown** does not mean unavailable.

Request part number and independent **UK** purchase channel for each; minimum quantity, stocked vs order-only, routine service replacement hours, technician qualification, OEM warranty policy, safety recommissioning test, UK replacement courier and RMA. Distinguish user-washable covers from user-replaceable safety-critical parts.

**Possible SENVEXA intersection — conditional only:** with manufacturer/dealer approval and appropriate qualified expertise, SENVEXA may develop **non-invasive documented post-service verification** of traction, repeatable floor transitions, acoustic drift, software version, diagnostic evidence chain and safe acceptance checks. This is a possible future technology/research validation wedge, **not a certified safety service or current revenue proposition**. Do not ask users to modify brakes or conduct hazardous live collision tests.

## 6. Short uniform OEM follow-up (no email sent)

> For **[specific SKU/firmware]** proposed for an occupied UK home: (1) provide third-party or calibrated OEM **LAeq/LAFmax** data for idle, walk/turn, ordinary-chair sit/rise and charging on tile/wood/carpet, specifying distance and structural vibration; (2) supply approved surface/threshold/carpet parameters and repeated-pass slip, scratching, wear and sole-replacement results; (3) supply child/pet-sized surrogate detection and protective-stop evidence, minimum recommended separation, fault/fall rescue and residential-use restrictions; (4) confirm UK pricing/availability, part numbers and lead times for shoes/soles, coverings, motors/joint seals, batteries, chargers and safety-relevant sensors; (5) identify exact safety standard edition, tests and any conformity assessment **without simply saying “ISO compliant”**. Please distinguish tested results from demonstrations and answer UNKNOWN where documentation is unavailable.

## 7. Boundaries and decision
- Family gate: independent safety outcome + one-person rescue + controlled child/pet exposure remains **P0**. **Do not weaken** the 2027-08 milestone criteria.
- Noise and cosmetic floors: **P1** for daily comfort and adoption; can become a practical home veto if no acceptable solution for the actual building.
- Wear/service: **P1** commercially. Insurance remains in its existing distinct memo; no duplicate study or claim that a public product automatically insures a particular model.
- No physical test, no pretend measurements, no supplier emails, no purchase, no list expansion. All results are desk-only **as of 2026-11-16**.
