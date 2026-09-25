---
title: "EvalLens core concepts"
description: "Definitions for projects, entries, batches, judge lenses, dimensions, AI scores, Jury Scores, Final Scores, spread and confidence."
status: generated
version: "0.2"
---

# EvalLens core concepts

The terms below follow one selection round from intake to ranking. The alphabetical list is the [Glossary](./glossary.md).

## Project and intake

- **Project** — one selection round: mode, criteria, weights, judges, entries, evaluations and reports.
- **Mode** — the panel and rubric chosen before setup. Pitch Competition: six judges and P1–P6. Hackathon: five reviewer roles and an execution-weighted rubric.
- **Entry** — one team's submission, details, deck and optional note. Status: `ready`, `incomplete` or `submitted`.
- **Batch** — all entries processed in one evaluation run.
- **Entry Hub** — the intake area for manual entry and public submissions.
- **Review Board** — the decision area for statuses, evidence, scores, comparison and the leaderboard.

## Panel terms

- **Judge lens** — one independent AI reviewer with a defined brief. The six pitch judges run in isolated contexts and never see one another's scores. See [AI judges](./scoring/judges.md).
- **Dimension** — one of the six questions P1–P6 used to compare pitch decks. See [Dimensions P1–P6](./scoring/dimensions.md).
- **Routing weight** — how much a judge counts toward a dimension: primary `1.00`, secondary `0.50`, advisory `0.25`, or not scored.
- **Confidence** — how well the evidence supports a read. Separate from judge disagreement.
- **Spread** — highest judge score minus lowest on one dimension. Under `1.5` is consensus, `1.5–2.99` a split, `3.0` or more a conflict. See [Disagreement and spread](./scoring/disagreement-and-spread.md).

## Score terms

| Score | Producer | Purpose |
|---|---|---|
| **AI Criterion Score** | AI panel | Read-only score for one dimension, with evidence |
| **AI Total Score** | Deterministic aggregation | Advisory reference across dimensions; never ranks the batch |
| **Jury Score** | Human reviewer | Score from `0.0` to `10.0` for one criterion |
| **Final Score** | Weighted calculation | Jury Scores combined with project weights; used for ranking |

If a ranking changes, a person changed a Jury Score or the project weighting. The AI Total Score never reorders the leaderboard.

## Evidence terms

- **Finding** — a signal that raises or lowers a dimension score and points to the slide behind it.
- **Deck completeness** — a check of ten sections: Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask and Other. `missing` means the deck did not cover it; it is not a fact-check.
- **Security signal** — raised when extraction finds an instruction aimed at the model inside a deck. The instruction is excluded from scoring evidence. See [Prompt-injection safety](./trust/prompt-injection-safety.md).

## Pipeline terms

Every deck passes five stages, in order:

1. **Decoder** — converts the input into a slide-level structure.
2. **AI Judges** — score the deck independently across the dimensions.
3. **Summarizer** — runs deterministic math and writes narrative questions.
4. **Scoring** — applies weights to produce the advisory AI Total Score and the human Final Score path.
5. **Report** — assembles the evidence-linked output.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Run an evaluation](./guides/run-an-evaluation.md) — The stages in practice {play}
- [Read a report](./guides/read-a-report.md) — Find each object in the output {file-text}
- [Score calculation](./scoring/how-the-score-is-built.md) — The arithmetic {sigma}

<!-- /widget -->
