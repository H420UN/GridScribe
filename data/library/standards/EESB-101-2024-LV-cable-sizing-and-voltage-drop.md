Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# LV cable sizing and voltage drop

| Title block | Detail |
|---|---|
| Document number | EESB-101 |
| Edition | 2024 |
| Status | Current |
| Date | 1 May 2024 |
| Scope | AC low-voltage cable sizing, origin-to-load voltage drop and ambient correction for fictional energy sites |

## 1. Purpose and application

This edition provides the fictional assessment basis for low-voltage AC feeders serving solar, storage and charging installations. It replaces EESB-101:2019 from 1 May 2024. The design record should identify the circuit function before choosing the applicable voltage-drop clause. A feeder supplying charging equipment is a power circuit even where the equipment is installed beside a public car park.

## 2. Design information

The calculation record should state the circuit identifier, supply origin, connected load, route length and destination. The recorded origin and destination should remain the same when alternative conductor sizes are compared. Where an intermediate distribution board is present, the complete origin-to-load path is relevant; a short final section should not conceal the contribution of the upstream feeder.

## 3. Cable selection record

The designer should retain the selected conductor arrangement and the assumptions used for load and installation conditions. Temperature correction and voltage drop are separate checks. Passing one does not demonstrate that the other has been addressed. Revised calculations should preserve a clear link to the circuit schedule so that a reviewer can distinguish a proposed correction from an issued design value.

## 4. Calculation presentation

Results should be expressed as a percentage of the nominal circuit voltage. Comparisons should use the calculated value before presentation rounding. The calculation sheet should distinguish the circuit category and identify the edition used for acceptance. A historic technical note can explain a method, but it does not replace the limits of this edition.

## 5.2. Power-circuit voltage drop

The maximum voltage drop from origin to load shall be **4% for power circuits, including EV charger feeders**. This applies to an AC feeder supplying an EV hub. The former 5% value in the 2019 edition is superseded and is not an alternative acceptance limit.

## 5.3. Lighting-circuit voltage drop

The maximum voltage drop from origin to load shall be **3% for lighting circuits**. Lighting should remain separately identifiable in a mixed site cable schedule. The power-circuit allowance shall not be substituted for the lighting limit.

## 6.1. Ambient temperature correction

Apply the following fictional derating factors for the stated design ambient temperature:

| Design ambient | Factor |
|---|---|
| 30 °C | 1.00 |
| 35 °C | 0.94 |
| 40 °C | 0.87 |
| 45 °C | 0.79 |

The ambient is the condition at the cable installation, not automatically the outside weather condition. An uncooled room can therefore require a different selection basis from an outdoor route.

## 7. Review evidence

Record the circuit value, relevant clause and comparison outcome together. If the route or load changes, revisit the calculation rather than copying the previous conclusion. DC string-to-inverter voltage drop is outside this document and is addressed separately in EESB-130:2022.
