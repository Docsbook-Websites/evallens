---
title: "Getting started with EvalLens"
description: "Set up a project, collect a batch, run the panel, inspect reports, and produce a leaderboard from human Jury Scores."
status: generated
version: "0.2"
---

# Getting started with EvalLens

Follow these steps to take one selection round from an empty project to a human-ranked leaderboard.

## Before you start

You need access through the limited partner program, a decision about the rubric, the submission field, and the people who will set Jury Scores.

Supported deck inputs are PDF, PPT, PPTX and Google Slides links. The current limit is one deck per team, up to 50 MB.

<!-- widget:stepper -->

### Open the workspace

Sign in with email and password or Google OAuth. Your workspace contains your projects and their status.

### Create the project

Choose the mode before the setup wizard opens. Pitch Competition uses six judges and dimensions P1–P6. Hackathon uses five reviewer roles and an execution-weighted rubric.

Complete the wizard for event details, criteria and weights, judges, collection, and final review.

### Choose intake

Add teams from the project page, publish a submission page, or use both methods. The [collection guide](./guides/collect-submissions.md) explains access rules and readiness statuses.

### Check the batch

Resolve incomplete entries before launching. Evaluation can start when at least one entry is ready; the run processes the ready batch in parallel.

### Run the evaluation

Launch the five stages: Decoder, AI Judges, Summarizer, Scoring and Report. See [Run an evaluation](./guides/run-an-evaluation.md).

### Inspect the reports

Open the Project Summary first, then the evidence and judge disagreement. Use the report's questions to prepare the live review.

### Set Jury Scores

In the Review Board, score each criterion from `0.0` to `10.0`. The AI Total Score is read-only and does not rank the batch.

### Generate the leaderboard

Generate the ranking after the human scores are submitted. The Final Score applies your criterion weights to the Jury Scores.

<!-- /widget -->

## What the run produces

- **Reports** — A summary, per-dimension analysis, evidence and live questions.
- **Completeness signals** — Present, thin or missing sections across ten core areas.
- **Review Board** — Status, scores, findings and comparison in one view.
- **Leaderboard** — A ranking based on human Jury Scores and project weights.

## Run a safe first test

Use a field that your team has already reviewed, such as last year's cohort. Compare the panel's evidence and ordering with the known result before changing your live process.

## Next steps

- [Core concepts](./concepts.md) — Learn the terms used across the reference.
- [Brief your jury](./guides/brief-your-jury.md) — Prepare reviewers before scoring.
- [What EvalLens does not do](./trust/boundaries.md) — State the product's limits clearly.
