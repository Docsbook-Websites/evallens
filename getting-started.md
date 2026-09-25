---
title: "Getting started with EvalLens"
description: "Set up a project, collect a batch, run the panel, inspect reports, and produce a leaderboard from human Jury Scores."
status: generated
version: "0.2"
---

# Getting started with EvalLens

These eight steps take one selection round from an empty project to a human-ranked leaderboard.

## Before you start

- **Access** — through the limited partner program; there is no public sign-up.
- **A rubric decision** — the criteria and weights your jury will use.
- **The submission field** — who applies and when the window closes.
- **Your jury** — the people who will set Jury Scores.

Decks arrive as PDF, PPT, PPTX or a Google Slides link: one deck per team, up to 50 MB.

<!-- widget:stepper -->

### Open the workspace

Sign in with email and password or Google OAuth. The workspace lists your projects and their status.

### Create the project

Choose the mode before the setup wizard opens: **Pitch Competition** (six judges, dimensions P1–P6) or **Hackathon** (five reviewer roles, an execution-weighted rubric). Then complete the wizard: event details, criteria and weights, judges, collection, final review.

### Choose intake

Add teams from the project page, publish a submission page, or both. See [Collect submissions](./guides/collect-submissions.md).

### Check the batch

Resolve incomplete entries. A run can start once at least one entry is `ready`, and it processes the ready batch in parallel.

### Run the evaluation

Launch the five stages: Decoder, AI Judges, Summarizer, Scoring and Report. See [Run an evaluation](./guides/run-an-evaluation.md).

### Inspect the reports

Open the Project Summary first, then the evidence and where judges disagreed. Take the report's questions into the live review.

### Set Jury Scores

In the Review Board, score each criterion from `0.0` to `10.0`. The AI Total Score is read-only and does not rank the batch.

### Generate the leaderboard

Generate the ranking once human scores are in. The Final Score applies your criterion weights to the Jury Scores.

<!-- /widget -->

## What the run produces

- **Reports** — a summary, per-dimension analysis, evidence and live questions.
- **Completeness signals** — present, thin or missing across ten core sections.
- **Review Board** — status, scores, findings and comparison in one view.
- **Leaderboard** — a ranking from human Jury Scores and project weights.

## Run a safe first test

<!-- widget:callout type=tip -->

Run your first project on a field your team already judged, such as last year's cohort. Compare the panel's evidence and ordering with the known result before it touches a live round.

<!-- /widget -->

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Core concepts](./concepts.md) — The terms used across the reference {compass}
- [Brief your jury](./guides/brief-your-jury.md) — Prepare reviewers before scoring {users}
- [What EvalLens does not do](./trust/boundaries.md) — The limits to state up front {shield-alert}
- [Trust and safety](./trust/README.md) — For your committee or IT office {shield}
- [Use cases](./use-cases/README.md) — How each kind of program sets up a round {trophy}

<!-- /widget -->
