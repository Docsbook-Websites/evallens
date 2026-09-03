---
title: "Run an EvalLens evaluation: the five pipeline stages"
description: "Launch a batch run and follow what happens to each deck — Decoder, AI Judges, Summarizer, Scoring, Report — plus what is parallel, what is deterministic, and what to check first."
---

# Run an evaluation

A run reads the whole batch, not one deck at a time. Decks are processed in parallel, so a cohort that would take a team weeks of reading comes back as a comparable set. The pace that matters afterwards is your review meeting, not processing time.

## Before you launch

- At least one entry is marked **ready**.
- Criteria and weights are what you want. **They lock when scoring starts**, so the whole field is ranked on one standard.
- Submissions are closed, or you accept that later arrivals belong to a second run.

## The five stages

Every deck follows the same fixed path. Nothing about the path changes between the first submission and the last, which is more than a room-based judging round can claim.

<!-- widget:stepper -->

### 01 · Decoder

A PDF, PPTX or Google Slides file becomes one structured, slide-level view. From here on, every judge reads the same representation of the deck — the format a team chose stops being a variable.

### 02 · AI Judges

The judges score the deck independently against the same criteria, in parallel, each in an isolated context. They do not see one another's scores, so there is no anchoring between lenses and an attack on one context cannot reach another.

Each judge cites the slide behind every claim, records what supports a higher band and what pulls toward a lower one, names the band, and only then picks a number inside it.

### 03 · Summarizer

Two separate functions. The first runs the deterministic math — no model call is involved in aggregating scores. The second writes the narrative and the follow-up questions to ask each team.

### 04 · Scoring

Your criterion weights are applied. Note which score they apply to: **weights combine with the human Jury Score to produce the Final Score.** The advisory AI Total Score is computed on the same weights but never orders the leaderboard.

### 05 · Report

An explainable report is assembled per participant: summary, per-dimension breakdown with evidence, judge contribution matrix, deck-completeness signals, and ranked questions for the live round.

<!-- /widget -->

## What is deterministic and what is not

This distinction matters when someone asks whether the score would come out the same tomorrow.

- **Aggregation is deterministic.** Once judge outputs exist, the score is calculated by a fixed function, not another model call. The same judge outputs and weights produce the same AI Total Score every time, within rounding tolerance.
- **The judge layer is measured.** Judges run on a language model, so repeated runs are not always identical. That repeatability is benchmarked rather than assumed — the published numbers are on [Reproducibility](../scoring/reproducibility.md).

## What to open first when the run finishes

Do not start at rank 1 and read down. Start where the report says to look:

1. **Conflicts.** Any dimension with a spread of 3.0 or more — the judges disagree, and averaging that is exactly the case a jury exists to discuss.
2. **High score, weak evidence.** Open the findings and check what actually supports the number.
3. **Critical completeness gaps.** A missing section flagged critical, and the dimension it drags on.
4. **Security signals.** A deck where an instruction aimed at the model was detected and excluded.

## Re-running and re-ranking

Criteria weights apply at the leaderboard, not inside each judge's reading. That means the same evidence can be re-ranked under different weights **without re-running the batch** — useful when a committee wants to see the field under a different emphasis. What you cannot do mid-round is change weights after scoring has started: the lock is what keeps the field comparable.

## Next steps

- [Read a report](./read-a-report.md) — the three layers and what each is for.
- [Disagreement and spread](../scoring/disagreement-and-spread.md) — what consensus, split and conflict mean numerically.
- [Score and shortlist](./score-and-shortlist.md) — turning reports into a ranking.
