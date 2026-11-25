Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Fen Edge Energy Hub — LV cable schedule

| Title block | Detail |
|---|---|
| Document number | FEH-EL-CS-001 |
| Edition | P01 |
| Status | Project — calculation summary for review |
| Date | 16 October 2026 |
| Scope | Origin-to-load AC voltage-drop results for selected LV power and lighting circuits |

## 1. Schedule basis

This schedule summarises the calculated voltage-drop results for the fictional Fen Edge Energy Hub, a 30 MW solar development for Fenland Power Co-operative. It is an extract for the design basis review rather than a procurement cable list.

The percentages below are origin-to-load AC results. Power circuits and the lighting circuit are identified separately because their acceptance limits differ. The schedule does not contain DC array string-to-inverter calculations.

## 2. Circuit summary

| Circuit | Function or route | Recorded route length | Calculated voltage drop | Circuit category |
|---|---|---|---|---|
| F1 | BESS auxiliaries | Not reproduced in this extract | 2.1% | AC power |
| F2 | Inverter room auxiliaries | Not reproduced in this extract | 3.2% | AC power |
| F3 | Main LV board to EV hub | 180 m | 4.6% | AC power |
| F4 | Site office supply | 140 m | 3.9% | AC power |
| F5 | CCTV and security supply | Not reproduced in this extract | 1.8% | AC power |
| L1 | Site lighting | Not reproduced in this extract | 2.7% | AC lighting |

Lengths not reproduced are outside the scope of this summary, not missing construction measurements or additional design defects.

## 3. F3 review item

F3 is the **180 m feeder from the main LV board to the EV hub**, with a calculated voltage drop of **4.6%**. This matches the project design inputs. It is an AC power feeder even though its destination equipment supplies vehicle charging.

Under EESB-101:2024, Clause 5.2, the power-circuit limit is 4%. F3 is the **only circuit in this schedule that fails its applicable voltage-drop limit**. Consider upsizing the cable or shortening or re-routing the feeder, then recalculate. No revised result is asserted here.

## 4. Other power circuits

F1, F2, F4 and F5 are below the current 4% power-circuit maximum. F4, at **3.9% over 140 m**, is a compliant near-limit result, not a second failure. Compare the recorded value with the actual limit rather than rounding it to a different conclusion.

The schedule does not use the 5% allowance quoted in historic WSP-TN-009:2021 and EESB-101:2019. That archived criterion is not the current acceptance basis.

## 5. Lighting circuit

L1 has a calculated voltage drop of **2.7%**. It satisfies the **3% lighting limit in EESB-101:2024, Clause 5.3**. The lighting result should remain labelled as lighting rather than being assessed under the more generous power-circuit allowance.

## 6. Calculation interfaces

The uncooled inverter-room basis is **40 °C with factor 0.87 applied**, as recorded in the design inputs. Ambient correction and voltage drop are separate checks. The **1.5% DC** allowance in EESB-130:2022, Clause 5.2, is not applicable to these AC results.

## 7. Revision handling

Retain this schedule as the P01 review basis. Label any proposed improvement as an option until selected, and update the circuit calculation and design inputs together when a change is adopted. Do not silently replace the recorded F3 result in the draft report.
