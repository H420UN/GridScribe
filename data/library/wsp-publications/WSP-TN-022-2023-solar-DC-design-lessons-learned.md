Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Solar DC design: lessons learned

| Title block | Detail |
|---|---|
| Document number | WSP-TN-022 |
| Edition | 2023 |
| Status | WSP note — current supporting commentary |
| Date | 15 September 2023 |
| Author role | Solar Electrical Design Specialist |
| Scope | String-sizing records, DC route coordination and avoiding confusion with AC feeders |

## 1. Review context

An earlier fictional array review found that design information was spread across a string schedule, a route drawing and a summary calculation. Each was understandable on its own, but different grouping names made the combined review harder than necessary. This note records the resulting documentation lessons.

The note supports the DC array standard. It does not establish a separate set of numerical design limits.

## 2. String sizing

Retain a clear relationship between the string arrangement and the voltage assessment. EESB-130:2022, Clause 4.1, sets a **maximum DC system voltage of 1500 V**. A total site capacity does not demonstrate the voltage of a string arrangement.

When the arrangement changes, update the schedule and calculation together. A revised module grouping should not remain associated with the previous calculation simply because the inverter destination has not changed.

## 3. Parallel arrangement

The number of parallel strings should be visible in the schedule. EESB-130:2022, Clause 4.6, requires string fuses where more than two strings are in parallel. The equipment grouping used for this review should agree with the grouping shown on the array drawing.

This is a distinct check from the maximum system voltage. A satisfactory voltage assessment does not establish the fuse provision for the selected parallel arrangement.

## 4. DC cable routing

Keep the route drawing linked to the string and inverter identifiers. A route change can affect the string-to-inverter calculation even when the equipment selection is unchanged. Record the route assumption used by the calculation, rather than relying on a later reader to reconstruct it from a revised plan.

Avoid merging unrelated circuits under a generic label such as “solar cables”. The reviewer needs to know which circuit result belongs to which route and destination.

## 5. Voltage-drop check

EESB-130:2022, Clause 5.2, sets the **maximum DC voltage drop from string to inverter at 1.5%**. State explicitly that this is a DC circuit assessment.

Do not apply the 1.5% value to an AC feeder supplying charging equipment. The current AC power-circuit allowance is found in EESB-101:2024, Clause 5.2. Identical clause numbers in different documents do not indicate identical subject matter.

## 6. Reporting lesson

A compact review table can list circuit grouping, destination, calculation reference and the relevant standard clause. Its purpose is to connect evidence, not to invent missing project inputs. Where a project pack contains only AC feeder data, do not manufacture a DC result to fill an unrelated report field.

## 7. Use of this note

Cite the standard for requirements and this note only for supporting explanation of the record structure. The main lesson is to preserve the distinction between array DC circuits and site AC distribution throughout drawings, schedules and the design basis report.
