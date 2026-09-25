---
title: "Run an EvalLens evaluation"
description: "Check readiness, launch a batch run, and understand the Decoder, AI Judges, Summarizer, Scoring and Report stages."
status: generated
version: "0.2"
---

# Run an EvalLens evaluation

A run processes the ready batch in parallel, through five stages. Check the rubric and intake first.

## Pre-flight checks

- At least one entry is marked `ready`.
- Criteria and weights are final; they lock when scoring starts.
- Submissions are closed, or later arrivals are deliberately left for another run.

<!-- widget:stepper -->

### Decoder

Converts a PDF, PPTX or Google Slides input into a structured, slide-level representation.

### AI Judges

Six independent [AI judges](../scoring/judges.md) score a pitch deck against the criteria in isolated contexts. Each records its evidence, what supports and lowers the score, and the band.

### Summarizer

Deterministic score calculations run first. A separate function writes the narrative and the questions for the live review.

### Scoring

The configured weights produce the advisory AI Total Score. The human Jury Score is a separate value, and it is the one the Final Score and leaderboard use.

### Report

Each participant gets a structured report: summary, dimension breakdown, evidence, judge contributions, completeness signals and ranked questions.

<!-- /widget -->

## Repeatable and variable parts of a run

Aggregation is deterministic once judge outputs and weights exist. The judge layer uses a language model, so a repeat can read differently; [Reproducibility](../scoring/reproducibility.md) gives the measured numbers.

## First checks after a run

1. **Conflicts** — a spread of `3.0` or more needs human discussion.
2. **High score with weak evidence** — open the cited findings.
3. **Critical completeness gaps** — check what the deck did not cover.
4. **Security signals** — confirm that instructions inside a deck were excluded from scoring evidence.

## Re-rank without re-running

Weights apply at the leaderboard, so after a run you can explore another weighting without collecting the evidence again.

<!-- widget:callout type=warning -->

**Weights stay fixed in a live round.** Changing them after scoring starts leaves a field ranked under two weightings, which is not one ranking.

<!-- /widget -->

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Read a report](./read-a-report.md) — Interpret the output {file-text}
- [Score and shortlist](./score-and-shortlist.md) — Set human scores {gavel}
- [Disagreement and spread](../scoring/disagreement-and-spread.md) — The review flags {git-compare}

<!-- /widget -->
