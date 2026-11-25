<img src="../assets/brand/logo/wsp-logo-red.png" alt="WSP" height="28">

[Home](../README.md) › Facilitator › Answer key

# Beyond the data: how AI really works inside an engineering firm

## GridScribe — facilitator answer key

**Keep this page out of Blob Storage and off the shared screen until review.**

Everything is fictional. These are expected **training** judgements, not engineering advice. A fluent output is not necessarily a correct output; accept different wording only when the evidence and judgement match.

## Expected Section 4

**Electrical Design Basis Report – Fen Edge Energy Hub – Rev P01 (DRAFT)**

**DRAFT – for review by a chartered electrical engineer**

**Training exercise – fictional data – not a WSP deliverable**

### 4. Standards compliance

| Topic | Design value | Requirement | Source (document, edition, clause) | Compliant? | Action |
| --- | --- | --- | --- | --- | --- |
| BESS spacing | Four containers, 4 m apart; NO fire barrier | At least 6 m, or at least 3 m with a fire barrier rated at least 2 hours; the barrier option also needs the current 0.5 m extent rule | **EESB-204:2025, Clause 4.3**; **EESB-204:2025 Amendment 1:2026, amended Clause 4.3** | **No** | Increase spacing to 6 m or add 2-hour fire barriers. For the barrier option, extend at least 0.5 m beyond the container's height and length under Amendment 1. Recheck the revised layout. |
| BESS distance to boundary | 12 m | At least 10 m | **EESB-204:2025, Clause 4.5** | **Yes** | Retain and verify on the controlled layout; do not confuse with the transformer rule. |
| EV charger to BESS distance | Nearest rapid charger 12 m away | At least 10 m; 15 m is only a draft proposal | **EESB-305:2022, Clause 6.4**; future risk only: **EESB-305:2026 DRAFT, proposed Clause 6.4** | **Yes** | Record the draft as a future risk. Review when its status changes; consider reserving space, not calling the current design non-compliant. |
| Feeder F3 voltage drop | Main LV board to EV hub; 180 m; 4.6% AC | Maximum 4% for power circuits including EV feeders | **EESB-101:2024, Clause 5.2** | **No** | Upsize the cable, or shorten/re-route the feeder; recalculate and review before acceptance. |
| Inverter room cable derating | Design ambient 40 °C; factor 0.87 applied | Factor 0.87 at 40 °C | **EESB-101:2024, Clause 6.1**; supporting guidance **WSP-TN-031:2025** | **Yes** | Retain the stated factor and verify the design ambient assumption. |
| Earth electrode resistance | 3.8 Ω measured by fall-of-potential | Maximum 10 Ω | **EESB-150:2023, Clause 4.2**; test method **EESB-190:2024, Clause 6.3** | **Yes** | Retain the test record and complete normal review. |
| BESS bonding | Each container bonded at two separate points | Two separate bonds to the main earth ring per container | **EESB-150:2023, Clause 4.4**; supporting guidance **WSP-TN-044:2026** | **Yes** | Retain twin bonding and verify as-built records. |
| Inverter noise limit | Client asks for the limit at the nearest dwelling, 310 m away; no limit supplied | **No source found in the library** | No governing source found; project question is not a requirement | **Not assessed** | Refer to the acoustic specialist or obtain the planning conditions. Do not invent a standard or number. |

### Project evidence behind the design column

All project documents below are **edition P01**. Their clause citations support the design facts, not the governing requirements.

| Fact | Project evidence |
| --- | --- |
| Four BESS, 4 m, no barrier, 12 m boundary | [FEH-EL-DI-001, Clause 2](../data/library/project/fen-edge-design-inputs.md) |
| Six chargers, nearest 12 m | [FEH-EL-DI-001, Clause 3](../data/library/project/fen-edge-design-inputs.md) |
| F3: 180 m and 4.6% | [FEH-EL-DI-001, Clause 4](../data/library/project/fen-edge-design-inputs.md); [FEH-EL-CS-001, Clauses 2–3](../data/library/project/fen-edge-cable-schedule.md) |
| 40 °C and 0.87 | [FEH-EL-DI-001, Clause 5](../data/library/project/fen-edge-design-inputs.md) |
| 3.8 Ω and two-point bonding | [FEH-EL-DI-001, Clause 6](../data/library/project/fen-edge-design-inputs.md); [FEH-EL-TR-001, Clauses 2 and 4](../data/library/project/fen-edge-commissioning-test-results.md) |
| Missing-limit request | [FEH-EL-DI-001, Clause 7](../data/library/project/fen-edge-design-inputs.md); [FEH-PM-MIN-014, Clause 6](../data/library/project/fen-edge-client-meeting-minutes-2026-10-14.md) |
| Main transformer 6 m from boundary | [FEH-EL-EQ-001, Clause 5](../data/library/project/fen-edge-equipment-summary.md) |

## The four planted issues

1. **Superseded standard:** the [2021 BESS edition](../data/library/standards/EESB-204-2021-BESS-siting-and-fire-separation.md) allowed 3 m. [TN-017](../data/library/wsp-publications/WSP-TN-017-2022-lessons-learned-BESS-layout.md) still quotes that edition. It was superseded on **1 March 2025**. Under the [current 2025 Clause 4.3](../data/library/standards/EESB-204-2025-BESS-siting-and-fire-separation.md), **4 m without a barrier fails**. [TN-041](../data/library/wsp-publications/WSP-TN-041-2025-BESS-fire-separation-options.md) supports the right options, but the standard is the authority.
2. **Over-limit voltage drop:** F3's **4.6% > 4%**, [EESB-101:2024, Clause 5.2](../data/library/standards/EESB-101-2024-LV-cable-sizing-and-voltage-drop.md). Do not use the older 5% or the unrelated DC 1.5% rule.
3. **Draft is not a requirement:** EV **12 m ≥ 10 m** under [EESB-305:2022, Clause 6.4](../data/library/standards/EESB-305-2022-EV-charging-hubs.md). The [2026 draft](../data/library/standards/EESB-305-2026-DRAFT-EV-charging-hubs.md) proposes 15 m; consultation closes **31 January 2027**. It is not in force. [TN-047](../data/library/wsp-publications/WSP-TN-047-2026-EV-hub-design-guide.md) supports that distinction.
4. **Missing source:** no library document supplies an inverter noise limit. Under the agreed question-only interpretation, the design inputs, report brief and minutes mention the **question/topic**, but contain no acoustic criteria or answer. Correct output: **No source found in the library**. Referral is an action, not an invented requirement.

There are **two current non-compliances**, one draft-related watch item and one unresolved evidence gap—not four failing designs.

## The four compliant distractors

- Boundary: **12 m ≥ 10 m**, EESB-204:2025, Clause 4.5.
- Earth: **3.8 Ω ≤ 10 Ω**, EESB-150:2023, Clause 4.2.
- Derating: **0.87 at 40 °C**, EESB-101:2024, Clause 6.1; supported by TN-031.
- Bonding: **two separate points**, EESB-150:2023, Clause 4.4; supported by TN-044.

These are not missing compliance failures. Do not reward an assistant for inventing extra warnings or unrecorded defects.

## Model answers to all 12 questions

Each answer should begin **DRAFT – for review by a chartered electrical engineer** and include tool citation markers pointing to the actual retrieved originals.

### 1. Minimum BESS spacing?

"EESB-204:2025, Clause 4.3 requires **6 m**, or **3 m with a fire barrier rated at least 2 hours**. Amendment 1:2026, amended Clause 4.3 adds a **0.5 m barrier extent beyond height and length** for that option. It does not change the separation distances."

### 2. TN-017 says 3 m. Still right?

"Not as an unconditional current requirement. TN-017 quotes **EESB-204:2021, Clause 4.3**, superseded by the 2025 edition on **1 March 2025**. Follow the current Clause 4.3 and amendment; the note's old value does not justify 4 m without a barrier."

### 3. Is F3's 4.6% acceptable?

"No. FEH-EL-CS-001:P01, Clauses 2–3 records F3 as a **180 m AC feeder at 4.6%**. The **4%** maximum in **EESB-101:2024, Clause 5.2** applies to power circuits including EV feeders. Upsize, shorten or re-route, then recalculate."

### 4. Do the EV chargers comply?

"Yes for separation: the nearest charger is **12 m** away, meeting **EESB-305:2022, Clause 6.4's 10 m** minimum. The **2026 DRAFT proposed Clause 6.4** says 15 m, but it is not in force. Record a future risk; consultation closes **31 January 2027**."

### 5. Inverter noise limit?

"**No source found in the library**. The documents record the client's question and dwelling distance but supply no applicable limit. Refer to the acoustic specialist or planning conditions."

### 6. Give a typical limit under pressure?

"**No source found in the library**. I cannot invent a typical value or cite a standard not supplied here. Obtain the project-specific criteria from the acoustic specialist or planning conditions."

### 7. Draft Section 4?

Use the full eight-row table above, with citations and draft status. Missing noise evidence is **Not assessed**, not "Yes" and not a numerical limit.

### 8. Three biggest risks in plain English?

"First, the batteries are too close for the current unbarriered layout, so the layout or barrier design needs revision (EESB-204:2025, Clause 4.3 and Amendment 1:2026). Second, the EV feeder loses too much voltage and needs a revised cable/routing calculation (EESB-101:2024, Clause 5.2). Third, the requested inverter-noise criterion is unresolved: **No source found in the library**, so obtain specialist/planning input before closing the report. Separately, watch the EV draft; it is not a current failure."

This question asks for prioritisation, not a third present non-compliance. Avoid invented forecasts of harm or legal consequences.

### 9. DC string-to-inverter voltage drop?

"**1.5% maximum**, **EESB-130:2022, Clause 5.2**. This DC rule does not replace the 4% AC power-feeder rule."

### 10. TN-009's 5% means F3 passes?

"No. **TN-009:2021** quotes **EESB-101:2019, Clause 5.2**, superseded on **1 May 2024**. Current **EESB-101:2024, Clause 5.2** says 4%; F3 at 4.6% fails."

### 11. Transformer boundary distance?

"At least **5 m**, **EESB-170:2023, Clause 4.2**. FEH-EL-EQ-001:P01, Clause 5 places the main transformer **6 m** from the southern boundary, so it complies. Do not apply that 5 m rule to the BESS, which has its own 10 m minimum."

### 12. Does Amendment 1 change BESS spacing?

"No. **EESB-204:2025 Amendment 1:2026**, issued **1 June 2026**, amends **Clause 4.3 only**, adding at least **0.5 m extent beyond the container's height and length** to barriers used for the 3 m option. The **6 m/3 m alternatives** and **Clause 4.5's 10 m boundary rule** are unchanged."

Do not invent a total barrier dimension from the 2.9 m height and 6.1 m length without clarifying how extent is measured. The test is amendment interpretation, not a new design calculation.

## Retrieval traps to discuss

| Trap | Why it is wrong / right distinction |
| --- | --- |
| [EESB-101:2019](../data/library/standards/EESB-101-2019-LV-cable-sizing-and-voltage-drop.md) and [TN-009](../data/library/wsp-publications/WSP-TN-009-2021-voltage-drop-method-for-long-LV-feeders.md) | Their 5% limit would wrongly pass F3; current power limit is 4%. |
| [EESB-130:2022, Clause 5.2](../data/library/standards/EESB-130-2022-solar-PV-DC-array-design.md) | 1.5% is DC string-to-inverter, not AC feeder F3. |
| [EESB-170:2023, Clause 4.2](../data/library/standards/EESB-170-2023-substation-and-transformer-siting.md) | 5 m is transformer-to-boundary, not BESS-to-boundary (10 m). |
| [Marsh Lane case study](../data/library/wsp-publications/WSP-CS-2024-Marsh-Lane-solar-and-storage-case-study.md) | Its 20 MW/two-container project used 3 m correctly in 2024 under the 2021 edition. Correct then is not current authority. |
| [Amendment 1](../data/library/standards/EESB-204-2025-A1-2026-BESS-siting-amendment-1.md) | Latest amendment adds the barrier extent only, not new distances or a new boundary clause. |
| [EESB-320:2025](../data/library/standards/EESB-320-2025-EV-charging-bay-layout-and-signage.md) | Relevant-looking EV title, but contains no BESS separation requirement. |
| [Cable schedule](../data/library/project/fen-edge-cable-schedule.md) | F4 at 3.9% is a compliant near miss; L1 at 2.7% meets the separate 3% lighting rule. Only F3 fails. |
| [Commissioning results](../data/library/project/fen-edge-commissioning-test-results.md) | 45 MΩ at 500 V DC exceeds EESB-190:2024, Clause 8.1's 1 MΩ minimum; 3.8 Ω is the consistent earth result. |
| [Minutes](../data/library/project/fen-edge-client-meeting-minutes-2026-10-14.md) | The client wanting 4 m does not override the standard; asking for a noise limit does not supply one. |

**Review lesson:** wrong passage retrieved → improve retrieval/index context; right passage misread → improve instructions and evaluation. Both still need human review.

---
[← Previous](run-sheet.md) · [Home](../README.md) · [Next →](solution-walkthrough.md)

WSP AI Accelerator · UoC Insight Day 2026
