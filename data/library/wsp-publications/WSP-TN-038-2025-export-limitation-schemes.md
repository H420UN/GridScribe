Fictional training document – created for the WSP GridScribe lab. Not a real standard or WSP publication. Not engineering guidance.

# Export limitation schemes

| Title block | Detail |
|---|---|
| Document number | WSP-TN-038 |
| Edition | 2025 |
| Status | WSP note — current supporting commentary |
| Date | 8 September 2025 |
| Author role | Grid Integration Engineer |
| Scope | Describing the export-control chain and linking design intent to test evidence |

## 1. Purpose

An export-limitation scheme is best described as a chain of functions rather than a collection of equipment names. This note suggests a record structure for a fictional energy-site review. It does not set a project export capacity or introduce a response criterion different from the current standard.

## 2. Establish the boundary

Start the functional description at the connection point and identify the plant participating in export control. On a combined solar and storage site, the description should make the relationship between the participating packages understandable. A controller listed in an equipment schedule does not, by itself, explain the full scheme.

Keep the connection-point identifier consistent between the single-line diagram, functional description and commissioning records. This prevents a measurement at one location being presented as evidence about another.

## 3. Response requirement

EESB-140:2025, Clause 3.3, requires the export limitation scheme to **respond within 5 seconds**. The report should cite that clause for the requirement and a project record for any observed response.

Describe the initiating condition and the resulting scheme response in the test narrative. Do not copy a product response claim into the report as if it were the observed response of the complete installed chain.

## 4. Interface review

List the measurement, control decision and participating plant functions in their operating sequence. Where separate packages meet, identify the interface in the coordinated description. Otherwise, each supplier description can appear complete while the overall relationship remains unclear.

This note does not prescribe additional settings or communication values. The objective is to keep the project evidence readable, not to fill absent settings with generic assumptions.

## 5. Separate related requirements

Connection-point power factor is addressed by EESB-140:2025, Clause 3.5, and loss-of-mains protection by Clause 6.1. Those are separate matters from the export response. A report should not use one successful check to imply that the others have been demonstrated.

Likewise, export limitation does not establish that an internal AC feeder meets its voltage-drop limit. Keep the grid-interface review and local circuit calculations separately traceable.

## 6. Revision control

If generation or storage participation changes, review the functional description against the revised arrangement. Retain the revision of the diagram used for the assessment. A test reference is less useful if its relationship to the tested plant arrangement is unclear.

## 7. Recommended report approach

Summarise the requirement, identify the relevant scheme boundary and reference the design or test evidence actually available. Clearly distinguish intended operation from observed operation. Cite EESB-140:2025, Clause 3.3, as the requirement source; use this technical note only to explain the recommended record structure. Do not infer a site-specific export-control result from this generic supporting note.
