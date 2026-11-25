Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Cable derating in hot inverter rooms

| Title block | Detail |
|---|---|
| Document number | WSP-TN-031 |
| Edition | 2025 |
| Status | WSP note — current supporting commentary |
| Date | 22 April 2025 |
| Author role | Electrical Cable Design Specialist |
| Scope | Recording ambient-temperature assumptions for cables in uncooled inverter rooms |

## 1. Why the assumption matters

An uncooled inverter room should not automatically inherit the outdoor temperature assumption used elsewhere on a site. The cable calculation needs an ambient appropriate to its installation location. A tidy calculation sheet can still be misleading if the temperature field has been copied from an unrelated circuit.

This note explains a fictional design-record approach. It supports the standard but does not introduce a separate acceptance criterion.

## 2. Recommended room basis

For an **uncooled inverter room, use a design ambient of 40 °C** in this training context. Apply the corresponding **0.87 derating factor from EESB-101:2024, Clause 6.1**.

Write both the ambient and factor into the cable design record. Recording only the factor makes it harder for a reviewer to understand the chosen basis; recording only the temperature leaves the applied correction unclear.

The recommendation concerns the surrounding condition for the cable assessment. It is not a requirement for battery-cell temperature or a description of a measured commissioning condition.

## 3. Practical record structure

A useful calculation summary names the circuit, the space it passes through and the ambient assumption adopted for that space. If the route includes different environments, describe the basis used rather than labelling the entire route simply “site”.

Keep the room description consistent with the project inputs. A note stating that the room is uncooled should not be paired with a calculation narrative that assumes cooling without identifying a design change.

## 4. Separate the checks

Ambient derating and voltage drop are separate checks. Applying the correct factor does not make an excessive voltage drop acceptable. Equally, a satisfactory voltage-drop result does not demonstrate that the ambient correction has been considered.

Use EESB-101:2024, Clause 5.2, for AC power-circuit voltage drop and Clause 6.1 for the ambient factor. The different clause references help the reviewer understand which part of the calculation supports each conclusion.

## 5. Common review misunderstanding

A reviewer may see 0.87 and assume it is a calculated efficiency or an adjustment made after testing. In this context it is the tabulated ambient correction factor associated with 40 °C. Describe it by name so that the design basis remains clear to a reader who has not seen the workbook.

Do not compare this room ambient with the battery-cell operating range in EESB-210:2024 as though the two refer to the same equipment condition.

## 6. Report wording

State the adopted room ambient and the factor actually applied, then cite EESB-101:2024, Clause 6.1. This note may be cited as supporting explanation, but the standard is the source of the factor. If the room arrangement changes, revisit the assumption rather than retaining the original factor simply because it appeared in an earlier calculation revision.
