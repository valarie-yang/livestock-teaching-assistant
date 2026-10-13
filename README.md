# Muzhi Livestock Teaching Assistant

An AI-assisted, teacher-side prototype for turning a teaching-case image into an editable question draft.

![Image-to-question authoring flow](https://raw.githubusercontent.com/valarie-yang/valarie-website/main/assets/muzhi-image-to-question-flow.svg)

**Current artifact:** The teacher authoring workflow is a local prototype. A student practice page is deployed separately, but the teacher's local question bank is not connected to it. This repository is a public-safe portfolio case; it does not contain the private product source.

## Product hypothesis

Teachers who already have teaching-case images may need to manually turn each image into a question, answer, and explanation before adding it to a practice bank. This is a product hypothesis, not a finding from user interviews or a measured classroom study.

## What the prototype does

1. A teacher selects an original or otherwise authorized teaching image.
2. The teacher may add an optional prompt to focus the learning objective.
3. After manually configuring a DeepSeek API, the prototype sends the selected image and prompt/context to that API to draft a candidate question, answer, and explanation. Use only original or authorized, non-sensitive materials, and review the provider's data terms before use.
4. The teacher edits and verifies the content, then saves it to the current browser's local question bank.

The product idea is to make an image-to-question workflow reviewable—not to publish generated content without a teacher.

## What is not connected or validated

- Image authoring requires a manually configured API and network access; the selected image and prompt/context leave the browser and are sent to the configured DeepSeek API.
- Reviewed questions are saved only in the current browser; they are not published to the online student practice page.
- Server-side teacher authoring and cross-device publishing are not deployed.
- Question quality, teacher time savings, classroom adoption, and learning outcomes have not been validated.
- This is for teaching practice only, not animal diagnosis or treatment guidance.

## Early API cost observation

Author-reported small-scale test mean: approximately **CNY 0.1 or less per question** for image recognition and question generation in the tested flow. The sample size and call scope are not standardized; actual costs vary with the model, image, prompt, and retries. This is not a benchmark or guarantee and excludes teacher review time.

## Product decisions and next validation

- Keep the image, optional learning focus, generated draft, teacher edits, and approval as distinct steps.
- Treat generated content as a candidate; teachers verify the question, answer, and explanation against authorized source material.
- Use original or authorized images in public materials; do not expose textbook/exam content, student records, API keys, logs, or private deployment details.
- Next, measure teacher review time, edit distance, and the share of drafts accepted after review. These are proposed measures, not current results.

## About the other learning-workflow materials

Some supporting documents in `docs/` describe a separate, synthetic learner-feedback case (learner reasoning, rubric feedback, teacher review, and remediation). That case is not the implementation of the image-to-question authoring demo described above. The documents remain useful as independent product-design work; do not conflate the two artifacts.

## Repository guide

- [Product brief](docs/product-brief.md) — the separate synthetic learning-workflow case
- [Workflow and review gates](docs/workflow-and-review-gates.md) — learner/teacher review-state design
- [Synthetic case set](docs/synthetic-case-set.md) — fictional examples only
- [Public data boundary](docs/public-data-boundary.md) — privacy, copyright, and safety limits
- [Portfolio evidence index](docs/portfolio-evidence-index.md) — evidence and recruiter reading path

This public repository is a curated portfolio case, not a mirror of the private application. It does not claim clinical validity, school deployment, or production-scale results.
