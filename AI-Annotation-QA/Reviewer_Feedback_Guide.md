# Reviewer Feedback Guide

## Feedback formula
**Case reference + observed issue + applicable rule + exact action requested + escalation note (if needed).**

## Examples
1. **Class mismatch — IMG-003:** The object is a motorcycle, but the current class is bicycle. Please update the class to motorcycle using the vehicle taxonomy.
2. **Missing object — IMG-002:** A pedestrian is visible near the right curb but has no annotation. Please add a person box if it meets the guideline's visibility threshold.
3. **Box too large — IMG-004:** The current box includes a large area of road. Please redraw it around the visible car according to the tight-box rule.
4. **Duplicate — IMG-005:** Two boxes represent the same parked car. Please remove the duplicate and retain one valid instance.
5. **Ambiguous class — IMG-007:** The object is too blurred to support a confident dog label. Please apply the approved unclear/ignore rule or flag it for QA Lead clarification.
6. **Track ID switch — VID-001:** The same red car changes from ID 12 to ID 19 without leaving the scene. Please use one consistent ID and inspect adjacent frames.
7. **Timestamp — VID-002:** The pedestrian is already visible at 00:04.2, but the event starts at 00:05.0. Please adjust the start time to the first qualifying frame if confirmed by the project rule.

## Handling disagreements
- Ask which guideline section informed the original decision.
- Compare the decision with the written rule and visual evidence.
- If the rule is clear, apply it consistently and explain the correction.
- If the rule is unclear or conflicting, escalate to the QA Lead or taxonomy owner and document the ruling.
- Share confirmed clarifications with affected annotators and reviewers.

## Avoid
- Blame or personal criticism.
- Vague notes without location or explanation.
- Invented thresholds or class rules.
- Closing unresolved disagreements without an owner decision.
