Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# LV protection and discrimination

| Title block | Detail |
|---|---|
| Document number | EESB-120 |
| Edition | 2024 |
| Status | Current |
| Date | 1 February 2024 |
| Scope | Protective-device coordination and protection interfaces at fictional EV charging hubs |

## 1. Application

This document provides fictional requirements for the protection review of low-voltage distribution arrangements. It covers the relationship between protective devices and the provision of protection at EV charging points. It does not set the voltage-drop allowance for the supplying cable or the spacing of chargers from BESS equipment.

## 2. System information

The protection record should identify the upstream supply, distribution boards and final charging points. Device identifiers should agree with the single-line diagram so that the reviewer can follow the path of a circuit. Equipment names used in a manufacturer schedule should be mapped to the project identifiers where the names differ.

## 3. Review boundaries

Protection, cable sizing and physical layout are related design activities, but their acceptance evidence is different. A current rating printed on a device is not evidence that discrimination has been reviewed. Similarly, a satisfactory separation on a site plan does not establish that each charging point has its required residual current protection.

## 4. Design record

The design record should identify the protective devices being compared and retain the selection evidence. When an upstream board arrangement changes, the reviewer should revisit the affected downstream relationships rather than assuming that a previous conclusion carries over unchanged.

The purpose of the record is to make the reasoning traceable, not simply to attach product literature without identifying which information supports the selected arrangement.

## 5.1. Protective discrimination

Discrimination shall be provided between **upstream and downstream protective devices**. The review should identify the paired devices and their positions in the distribution arrangement. A general statement that the site has protection does not describe the required relationship between those devices.

The design basis should summarise the reviewed arrangement and reference its supporting assessment. This clause does not supply a project-specific device setting; settings remain part of the selected equipment design record.

## 6. Change control

Changes to charging equipment or board allocation should be reflected in the protection schedule. Keep the revision of the single-line diagram consistent with the protection review. A displaced circuit label can make otherwise valid evidence difficult to apply to the correct charging point.

## 7.2. EV charging-point residual current protection

Each EV charging point shall have its **own 30 mA residual current protection suitable for DC fault currents**. The record should identify the protection for each point separately. A common descriptive note for a hub should not obscure whether the requirement has been addressed at every point.

## 7.5. EV board surge protection

Surge protection shall be provided at the **EV hub distribution board**. The equipment schedule should identify the board and the associated provision so that the report does not confuse it with protection installed elsewhere on the site.

## 8. Reporting interface

Use this document for protection requirements and cite the relevant clause. Use EESB-101:2024 for AC voltage drop and EESB-305:2022 for charger-to-BESS separation. Keeping those sources separate makes each compliance statement easier to verify.
