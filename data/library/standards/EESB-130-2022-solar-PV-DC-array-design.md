Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Solar PV DC array design

| Title block | Detail |
|---|---|
| Document number | EESB-130 |
| Edition | 2022 |
| Status | Current |
| Date | 1 June 2022 |
| Scope | Solar-array DC voltage, parallel-string fusing and string-to-inverter DC voltage drop |

## 1. Application

This fictional standard addresses the DC side of a photovoltaic installation, from strings towards the inverter input. Its voltage-drop allowance is not the allowance for an AC feeder supplying an EV hub. The distinction between circuit functions should remain visible in schedules, calculations and report citations.

## 2. Circuit identification

The design record should identify the array grouping, string arrangement and inverter destination. A DC circuit identifier should be distinguishable from the identifiers used for site auxiliary power and lighting. Where calculations are exported into a common workbook, the circuit type should remain visible on each result sheet.

## 3. Design inputs

The review should retain the selected equipment arrangement and the assumptions used for string and cable calculations. Changes to the number of parallel strings should be communicated to the protection review. Changes to the route should be reflected in the string-to-inverter calculation rather than left only on a civil drawing.

## 4.1. Maximum DC system voltage

The maximum DC system voltage shall be **1500 V**. The calculation record should identify the DC system being assessed. This voltage is a limit for the array design and is not a statement of the nominal AC supply to site equipment.

The reviewer should be able to trace the selected string arrangement to the voltage assessment. A plant capacity stated in megawatts does not establish the voltage of an individual DC circuit.

## 4.6. Parallel-string fusing

String fuses shall be provided where **more than two strings are connected in parallel**. The design record should state the parallel arrangement explicitly so that the applicability of this clause is clear. A total module count alone does not describe the number of parallel strings.

The protection schedule should use the same grouping identifiers as the array drawing. This helps avoid applying evidence for one grouping to another after a layout change.

## 5.2. DC voltage drop

The maximum **DC voltage drop from string to inverter shall be 1.5%**. Record both endpoints and the DC circuit designation with the result. This limit does **not** apply to the AC supply feeder from a main LV board to an EV hub.

For AC power-circuit voltage drop, consult EESB-101:2024, Clause 5.2. Both documents contain a Clause 5.2, so the document number and edition are essential parts of a useful citation. A clause number without its source is not an adequate identifier.

## 6. Review and reporting

Keep system voltage, string-fuse provision and DC voltage drop as separate checks. Do not describe a feeder as acceptable merely because it satisfies a limit intended for another circuit category. Supporting lessons-learned notes can explain how to organise the evidence, but the requirement should be attributed to this standard and the relevant clause.
