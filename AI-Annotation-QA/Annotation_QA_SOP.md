# Annotation QA Standard Operating Procedure (SOP)

**Portfolio case study | Simulated training exercise**

## Purpose
Provide a repeatable method for reviewing image and video annotations before acceptance.

## Scope
This SOP is a simulated portfolio template. Real projects must align it with their client instructions, tool schema, and acceptance criteria.

## Inputs
- Source image/video and annotation output.
- Current guideline and taxonomy version.
- Project-specific box, visibility, tracking, attribute, and timestamp rules.
- Audit log and escalation route.

## Procedure
1. Confirm the task, file version, guideline version, and review scope.
2. Inspect object completeness, labels, boxes, attributes, tracks, timestamps, and rule compliance.
3. Record each defect with a case ID and evidence/location or timestamp.
4. Classify the error and assign severity based on impact and recurrence.
5. Approve correct items; return supported defects for correction; escalate ambiguity or missing rules.
6. Verify corrections and close the audit record.

## Decision rules
- **Approve:** all required checks pass within the defined review scope.
- **Return for correction:** a specific defect and correction are supported by guideline and evidence.
- **Escalate:** source evidence is incomplete or the guideline is ambiguous or conflicting.
- **Reject:** use only where the actual project has a documented rejection rule.

## Escalation
Escalate taxonomy gaps, conflicting interpretations, unclear visibility thresholds, unresolved identity questions, and repeated systemic defects to the QA Lead or designated owner.

## Documentation
Retain guideline version, case ID, issue, evidence location, category, severity, decision, feedback, correction status, and final closure.
