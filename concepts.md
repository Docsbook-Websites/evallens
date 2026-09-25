---
title: "EvalLens core concepts"
description: "Definitions for projects, entries, batches, judge lenses, dimensions, AI scores, Jury Scores, Final Scores, spread and confidence."
status: generated
version: "0.2"
---

# EvalLens core concepts

The terms below follow one selection round from intake to ranking.

## Project and intake

**Project** — One selection round. It contains the mode, criteria, weights, judges, entries, evaluations and reports.

**Mode** — The panel and rubric selected before setup. Pitch Competition uses six judges and P1–P6. Hackathon uses five reviewer roles and an execution-weighted rubric.

**Entry** — One team's submission, details, deck and optional note. Its status is `ready`, `incomplete` or `submitted`.

**Batch** — All entries processed in one evaluation run.

**Entry Hub** — The intake area for manual entry and public submissions.

**Review Board** — The decision area for statuses, evidence, scores, comparison and the leaderboard.

## Panel terms

**Judge lens** — One independent AI reviewer with a defined brief. The six pitch judges run in isolated contexts and do not see one another's scores.

**Dimension** — One of the six questions P1–P6 used to compare pitch decks.

**Routing weight** — How much a judge contributes to a dimension: primary `1.00`, secondary `0.50`, advisory `0.25` or not scored.

**Confidence** — A signal describing how well the evidence supports a read. It is separate from judge disagreement.

**Spread** — The highest judge score minus the lowest on one dimension. Under `1.5` is consensus, `1.5–2.99` is a split, and `3.0` or more is a conflict.

## Score terms

| Score | Producer | Purpose |
|---|---|---|
| **AI Criterion Score** | AI panel | Read-only score for one dimension, with evidence |
| **AI Total Score** | Deterministic aggregation | Advisory reference across dimensions; never ranks the batch |
| **Jury Score** | Human reviewer | Score from `0.0` to `10.0` for one criterion |
| **Final Score** | Weighted calculation | Human Jury Scores combined with project criteria weights; used for ranking |

If a ranking changes, a person changed the Jury Score or the project weighting. The AI Total Score does not directly reorder the leaderboard.

## Evidence terms

**Finding** — A signal that raises or lowers a dimension score and points to the slide that supports it.

**Deck completeness** — A check of ten sections: Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask and Other. `missing` means the deck did not cover the section; it is not a fact-check.

**Security signal** — A flag raised when the extraction stage finds an instruction aimed at the model inside a deck. The instruction is excluded from scoring evidence.

## Pipeline terms

Every deck passes five stages:

1. **Decoder** — Converts the input into a slide-level structure.
2. **AI Judges** — Scores the deck independently across the dimensions.
3. **Summarizer** — Runs deterministic math and writes narrative questions.
4. **Scoring** — Applies weights to produce the advisory AI Total Score and the human Final Score path.
5. **Report** — Assembles the evidence-linked output.

## Next steps

- [Run an evaluation](./guides/run-an-evaluation.md) — Follow the stages in practice.
- [Read a report](./guides/read-a-report.md) — Find each object in the output.
- [Score calculation](./scoring/how-the-score-is-built.md) — Review the arithmetic.
