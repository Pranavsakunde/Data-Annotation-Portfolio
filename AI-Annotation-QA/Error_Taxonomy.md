# Annotation QA Error Taxonomy

| Category | What to check | Example |
|---|---|---|
| Missing annotation | Required object/event absent | Visible pedestrian has no box |
| Labeling error | Incorrect class or taxonomy mapping | Motorcycle labeled bicycle |
| Bounding box error | Box too large, small, or misplaced | Car box includes excessive road |
| Duplicate annotation | Same target represented more than once | Two boxes cover one parked car |
| Attribute error | Unsupported or incorrect attribute | Blue sign tagged red |
| Ambiguity / insufficient evidence | Label cannot be supported | Blurred distant shape guessed as a dog |
| Track identity error | Object ID changes or is assigned incorrectly | Same car changes track ID |
| Timestamp error | Start/end boundary is inaccurate | Event begins after first qualifying frame |
| Guideline / taxonomy gap | Instructions are missing or conflicting | No rule for a new object type |
| Metadata / format error | Required schema or metadata is invalid | Missing required field |

## Severity guidance
- **Critical:** likely to invalidate a meaningful portion of the dataset or create severe downstream risk.
- **Major:** materially affects a label, object, track, event, or required rule and must be corrected before approval.
- **Minor:** limited, low-impact defect that still needs correction if the schema requires it.

Severity depends on task context, frequency, and downstream impact. These are training defaults, not universal industry thresholds. Use the project's own severity matrix when available.

## Decision principles
- Approve correct work; do not manufacture defects.
- Return supported defects with precise corrective action.
- Escalate unclear rules or insufficient source evidence.
- Expand review when a defect suggests a recurring or systemic pattern.
