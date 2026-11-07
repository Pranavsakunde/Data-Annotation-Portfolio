# Image & Video Annotation QA Checklist

Use the actual approved project guideline as the source of truth. If a criterion is undefined, document the gap and escalate rather than inventing a rule.

## Image annotation
- [ ] All in-scope visible objects are annotated, including relevant edge and partially occluded objects.
- [ ] Each object uses an approved class from the taxonomy.
- [ ] Bounding boxes follow the project's tightness, padding, truncation, and occlusion rules.
- [ ] No duplicate boxes represent the same physical object unless explicitly required.
- [ ] Attributes use allowed values and are supported by visible evidence.
- [ ] Ambiguous or blurred objects use the approved unknown/ignore rule or are escalated.
- [ ] Required metadata and file identifiers are complete.
- [ ] Equivalent objects are labeled consistently across the batch.

## Video annotation
- [ ] Object tracks maintain identity across frames according to continuity and occlusion rules.
- [ ] IDs are not switched between objects or reused for simultaneous objects.
- [ ] Required objects are present throughout the applicable interval.
- [ ] Start/end timestamps match the first and last qualifying frames.
- [ ] Actions/events are supported by the full interval, not inferred from one isolated frame.
- [ ] Frame-level boxes and attributes follow image annotation rules.
- [ ] Unclear identity or event boundaries are documented and escalated.

## Review decision
- [ ] Approve when all required checks pass within the defined review scope.
- [ ] Return for correction when a specific defect and correction are supported by evidence and the guideline.
- [ ] Escalate when rules conflict, are missing, or evidence is insufficient.
- [ ] Reject only when the actual project defines rejection criteria.

## Audit record
Record case ID, guideline version, issue, evidence/location or timestamp, category, severity, decision, feedback, correction status, and closure.
