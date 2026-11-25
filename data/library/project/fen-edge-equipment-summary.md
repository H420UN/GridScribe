Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Fen Edge Energy Hub — equipment summary

| Title block | Detail |
|---|---|
| Document number | FEH-EL-EQ-001 |
| Edition | P01 |
| Status | Project — equipment design summary |
| Date | 16 October 2026 |
| Scope | Principal equipment counts, container envelopes and supporting design provisions |

## 1. Project equipment basis

This summary describes the fictional Fen Edge Energy Hub for Fenland Power Co-operative in Cambridgeshire. The scheme comprises a **30 MW solar farm**, battery storage and a public rapid-charging hub. Equipment quantities in this document belong to Fen Edge, not to the historic Marsh Lane case study.

The summary supports the design inputs and does not silently revise the layout or the F3 calculation.

## 2. BESS containers

| Attribute | Design description |
|---|---|
| Container identifiers | BESS-01, BESS-02, BESS-03, BESS-04 |
| Quantity | Four |
| Energy capacity | 5 MWh per container |
| Container length | 6.1 m |
| Container height | 2.9 m |
| Inter-container spacing | 4 m |
| Fire barrier | None |
| Site boundary distance | 12 m |
| Main earth-ring connections | Two separate points per container |

Gas detection is provided in every container, consistent with EESB-204:2025, Clause 5.1. Thermal management is specified to maintain battery cells within EESB-210:2024, Clause 5.2, and vent discharge is oriented away from walkways and access routes under Clause 6.3.

The container envelope is included to support layout review. No barrier dimensions are stated because no barrier is part of this design.

## 3. EV charging equipment

The hub has **six 150 kW rapid chargers**, serving six bays beside the public car park. The nearest charger is **12 m from a BESS container**.

Each charging point has its own 30 mA residual current protection suitable for DC fault currents, and surge protection is provided at the EV hub distribution board, consistent with EESB-120:2024, Clauses 7.2 and 7.5. An emergency stop is within sight of every bay under EESB-305:2022, Clause 6.6.

Bay dimensions, the accessible bay and the tariff, contact and stop-location signs meet the provisions in EESB-320:2025. These provisions do not determine the charger-to-BESS separation.

## 4. Inverters and electrical rooms

There are **two central inverters** in the uncooled inverter-room arrangement. The cable design basis is **40 °C with factor 0.87 applied**. Automatic fire detection covers the inverter and switch rooms, with alarms relayed to a 24/7 remote monitoring centre in accordance with EESB-180:2022.

Protective discrimination is included in the coordinated LV design under EESB-120:2024, Clause 5.1.

## 5. Transformer and substation

The main transformer is **33/0.4 kV**, associated with the **33 kV substation**, and is **6 m from the southern site boundary**. This satisfies the **5 m transformer clearance in EESB-170:2023, Clause 4.2**. Oil containment is sized to the 110% provision in Clause 4.4.

## 6. Supporting design interfaces

The cable installation design follows EESB-110:2023 for burial, warning tape and shared-trench separation. The grid interface includes export response, power-factor provision and loss-of-mains protection in accordance with EESB-140:2025. The site lightning assessment and selected protection follow EESB-160:2024, with the lightning protection system bonded to the main earth ring.

## 7. Report boundary

These supporting provisions do not remove the need to assess the recorded BESS spacing or F3 voltage drop separately. Use the project design inputs and current clauses for those conclusions.
