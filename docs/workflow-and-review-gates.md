# Workflow and review gates

## Learner states

`CASE_OPEN → RESPONSE_DRAFT → RESPONSE_SUBMITTED → FEEDBACK_READY → REMEDIATION_ASSIGNED → REMEDIATION_COMPLETE`

## Teacher states

`UNREVIEWED → REVIEW_REQUIRED → APPROVED_FOR_LEARNING → RETURNED_FOR_REVISION`

`APPROVED_FOR_LEARNING` means the feedback can be used in the learning workflow. It does not mean the content is a clinical recommendation or an institutional curriculum approval.

## Review triggers

- missing observation evidence;
- conflict between observation and conclusion;
- low confidence or incomplete reasoning;
- unsafe or clinically overconfident language;
- generated content that cannot be traced to the synthetic case rubric;
- content awaiting human approval before release.

## AI boundary

The AI layer is limited to draft organization, rubric-linked feedback, and remediation suggestions. Deterministic rubric rules and teacher review control the final learning status. The system does not diagnose animals, prescribe treatment, publish content, or make decisions about real animals.
