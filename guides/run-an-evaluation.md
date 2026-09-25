---
title: "Run an EvalLens evaluation"
description: "Check readiness, launch a batch run, and understand the Decoder, AI Judges, Summarizer, Scoring and Report stages."
status: generated
version: "0.2"
---

# Run an EvalLens evaluation

A run processes the ready batch in parallel. Before launching, confirm that the rubric and intake are ready.

## Pre-flight checks

- At least one entry is marked **ready**.
- Criteria and weights are final; they lock when scoring starts.
- Submissions are closed, or later arrivals are intentionally reserved for another run.

<!-- widget:stepper -->

### Decoder

The system converts a PDF, PPTX or Google Slides input into a structured, slide-level representation.

### AI Judges

Six independent judges score a pitch deck against the criteria in isolated contexts. Each judge records evidence, what supports the score, what lowers it, and the relevant band.

### Summarizer

Deterministic score calculations run first. A separate function writes the narrative and questions for the live review.

### Scoring

The configured weights produce the advisory AI Total Score. The human Jury Score is a separate value and is the value used for the Final Score and leaderboard.

### Report

Each participant receives a structured report with a summary, dimension breakdown, evidence, judge contributions, completeness signals and ranked questions.

<!-- /widget -->

## Repeatable and variable parts of a run

Aggregation is deterministic once the judge outputs and weights exist. Repeating the judge layer can produce different reads because it uses a language model; [Reproducibility](../scoring/reproducibility.md) describes what is measured.

## First checks after a run

1. **Conflicts** — a spread of `3.0` or more needs human discussion.
2. **High score with weak evidence** — open the cited findings.
3. **Critical completeness gaps** — check what the deck did not cover.
4. **Security signals** — confirm that instructions inside a deck were excluded from scoring evidence.

## Re-rank without re-running

Weights apply at the leaderboard. You can explore a different weighting after a run without re-running the evidence collection. Do not change weights after scoring starts for the live round.

## Next steps

- [Read a report](./read-a-report.md) — Interpret the output.
- [Score and shortlist](./score-and-shortlist.md) — Set human scores.
- [Disagreement and spread](../scoring/disagreement-and-spread.md) — Understand the review flags.
