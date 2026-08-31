# Public-safe product decisions

This document distills the reviewed private teaching-agent baseline into a public portfolio artifact. It intentionally excludes private platform configuration, textbook files, recovered exam questions, real learner records, credentials, internal URLs, and institution-specific deployment details.

## Product scope

The product is an AI-assisted learning workflow for livestock and veterinary teaching. It helps learners connect observation, reasoning, evidence, and prevention planning. It helps teachers review reasoning, identify low-confidence cases, and assign targeted remediation.

It is educational assistance, not a veterinary diagnostic or treatment system.

## Learning workflow

```
Case observation
  → Learner hypothesis and reasoning
  → Evidence and rubric review
  → AI feedback draft
  → Teacher review and release
  → Remediation or spaced practice
  → Progress view
```

The system is designed around the teaching decision that follows an answer. An AI explanation is useful only when a teacher or learner can inspect the evidence, correct the reasoning, and choose the next learning action.

## Product decisions

1. The teacher owns publication of feedback and learning content.
2. Low-confidence, contradictory, incomplete, or weakly supported answers enter a review queue.
3. Evidence is separated from the model's narrative so a teacher can check why a suggestion was produced.
4. Remediation is a product state, not a generic “try again” message; it is linked to the weak concept or reasoning step.
5. Content provenance and review status are tracked separately from learner performance.
6. Platform limitations do not justify exposing private material or presenting an unverified configuration as a production release.
7. Synthetic cases are used in the public portfolio package to demonstrate the workflow without publishing copyrighted teaching materials or real learner data.
8. The public product boundary excludes autonomous diagnosis, treatment prescription, official academic decisions, and claims of clinical or school outcomes.

## Review states

```
Draft case
  → Content review
  → Approved for demonstration
  → Learner attempt
  → AI feedback draft
  → Teacher review
  → Released feedback
  → Remediation assigned
```

A case or feedback item that has not passed its required review gate is not treated as authoritative course content.

## Public evidence and limits

The public repository demonstrates product framing, workflow design, review gates, content governance, and a synthetic demonstration package. It does not mirror the private source project and does not claim an official school deployment, clinical validity, or production teaching outcomes.

The private source baseline was used to sharpen the public product case; private platform assets and source content remain private.
