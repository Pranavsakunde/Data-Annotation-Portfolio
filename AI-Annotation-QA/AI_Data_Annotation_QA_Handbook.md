# AI Data Annotation Quality Assurance Handbook

**Portfolio case study | Simulated training exercise | No client data used**

## Project overview
This no-code case study demonstrates a structured quality assurance workflow for human-created image and video annotations. It focuses on checking annotation outputs against approved rules, classifying defects, making review decisions, documenting feedback, and escalating cases where evidence or guidelines are insufficient.

All 30 audit cases and example findings are simulated. They are not client work, production audit results, or claims about an employer's internal process.

## What is annotation QA?
Annotation QA is the controlled review of labeled data against an approved annotation guideline. A reviewer checks whether labels, boxes, attributes, timestamps, and object identities are accurate and consistent.

## Why it matters
- Incorrect labels can teach a model the wrong relationship between an input and its expected output.
- Inconsistent labels make equivalent objects or events appear different in training data.
- Late defect discovery creates rework, delays, and avoidable quality risk.

## Roles
- **Annotator:** creates labels according to the current guideline.
- **Reviewer:** checks submitted work, records evidence, and approves, returns, or escalates.
- **QA Lead:** owns guideline interpretation, reviewer calibration, recurring quality issues, and unresolved edge cases.

## Reviewer principles
- Follow the approved guideline, not personal preference.
- Check completeness as well as correctness.
- Record evidence and exact correction details.
- Use consistent severity criteria.
- Approve correct work; do not invent defects.
- Escalate unclear instructions or insufficient evidence.
- Keep an auditable record of decisions and unresolved questions.

## Scenario analysis
A hypothetical team labels 500 street images for a vehicle detector. Some annotators label auto-rickshaws as “car” and others as “other.” A reviewer spot-checks 10 images, sees no issue, and approves the batch. Later, the model confuses rickshaws with cars.

This is an inconsistent-labeling problem and possibly a taxonomy gap. A small spot-check may not be representative or targeted at rare vehicle types. The reviewer should inspect the approved taxonomy, compare similar examples across the batch, expand review when risk is found, and return affected items. The QA Lead or taxonomy owner should decide the mapping with the project owner if the guideline is unclear.

## Review dimensions
- Object presence and completeness.
- Class label and taxonomy compliance.
- Bounding-box geometry.
- Duplicate instances.
- Attributes and metadata.
- Ambiguity and evidence sufficiency.
- Video track identity and continuity.
- Timestamp and event boundaries.
- Consistency across equivalent cases.

## Severity
- **Critical:** likely to invalidate a meaningful portion of the dataset or create severe downstream risk.
- **Major:** materially affects a label, object, track, event, or required rule and needs correction before approval.
- **Minor:** limited, low-impact defect that still needs correction if the schema requires it.

Severity depends on context, frequency, and downstream impact. These examples are training defaults, not universal thresholds.

## Review workflow
Receive task → confirm guideline/version → inspect required scope → log defects → classify severity → decide approve/return/escalate → communicate feedback → verify correction → close and retain audit record.

## Limitations
- The 30-case sample is simulated and illustrative.
- Real projects require access to actual task guidelines and source media.
- No inter-annotator agreement or reviewer calibration statistic is claimed because no independent second reviewer participated.
- Some examples require project-specific rules. Escalation is appropriate when the guideline or evidence is insufficient.
