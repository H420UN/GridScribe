Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Voltage-drop method for long LV feeders

| Title block | Detail |
|---|---|
| Document number | WSP-TN-009 |
| Edition | 2021 |
| Status | WSP note — historic; acceptance value OUTDATED |
| Date | 12 March 2021 |
| Author role | LV Network Design Engineer |
| Scope | Organisation of long-feeder calculations, with an archived acceptance reference |

## 1. Background

Long feeders are sensitive to route changes that can be easy to overlook when a site plan develops. This note originally described a way to keep the route, load and conductor assumptions together on a calculation sheet. Its original acceptance reference is now outdated, although the record-keeping lesson remains useful.

## 2. Define the circuit

Identify the supply origin, destination and circuit function before recording a route length. The length should relate to the actual route assumption, not simply the straight-line distance between equipment symbols. Keep the origin-to-load boundary visible so that later revisions compare like with like.

If an intermediate board is introduced, retain enough information to understand the full path rather than allowing a short downstream section to stand in for the whole circuit.

## 3. Original acceptance statement — OUTDATED

The original note stated: **“a 5% limit applies (EESB-101:2019 Clause 5.2)”**. This was the historic power-circuit limit.

**Do not use that value for current acceptance.** EESB-101:2019 was superseded by EESB-101:2024 on 1 May 2024. The current Clause 5.2 limits power circuits, including EV charger feeders, to 4% from origin to load.

An inherited workbook can therefore produce an unchanged result while its old pass indication becomes wrong under the current criterion. Review the acceptance field as well as the arithmetic.

## 4. Compare alternatives consistently

When considering a larger conductor or a revised route, keep unchanged assumptions clearly identified. State which input changed and record the revised result against the same circuit identifier. A proposed alternative should not overwrite the issued design value before the change is selected.

The useful comparison is between traceable options. A lower percentage without a clear origin, destination and route assumption is not enough to explain how the improvement would be achieved.

## 5. Keep related checks distinct

Cable ambient derating is separate from voltage drop. The current ambient factors are in EESB-101:2024, Clause 6.1. A feeder does not gain a more generous voltage-drop allowance because the correct temperature factor has been applied.

Likewise, the DC string-to-inverter limit in EESB-130:2022 is not a limit for an AC feeder. Identify the circuit category before selecting the source.

## 6. Review conclusion

Use this note only as supporting history for a calculation method. Cite EESB-101:2024, Clause 5.2, for the present AC power-circuit limit. In particular, a 4.6% feeder result would pass the old 5% comparison but fails the current 4% comparison. Do not retain the old pass conclusion merely because it appears in a familiar calculation template.
