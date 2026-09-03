---
title: "EvalLens core concepts: projects, judges, dimensions and the three scores"
description: "The vocabulary of an EvalLens run — project, entry, batch, judge lens, dimension, AI Criterion Score, AI Total Score, Jury Score, Final Score, spread and confidence."
---

# Core concepts

EvalLens uses three different scores and they are not interchangeable. This page defines every term the rest of the documentation relies on, in the order the objects appear in a run.

## The objects

**Project.** One selection round: a competition, a cohort intake, an open call, a hackathon. A project carries its own mode, criteria, weights, judges and intake settings. In the current release each project belongs to one organizer, who owns its decks, evaluations and reports.

**Mode.** Chosen before the setup wizard opens, and it determines the panel. *Pitch Competition* runs six judges against dimensions P1–P6. *Hackathon* runs five reviewer roles against an execution-weighted rubric.

**Entry.** One team's submission: the pitch deck, the team and project details, and an optional note for the jury. Every entry follows the same structure, so judging starts from consistent data. An entry has a status — ready, incomplete, or submitted.

**Batch.** All entries in a project, evaluated in one run rather than deck by deck.

**Entry Hub.** The intake side of the product: manual entry, or a public submission page with its own access rules and window.

**Review Board.** The decision side: the whole batch in one view, with statuses, scores, findings and the leaderboard.

## The panel

**Judge lens.** One of six independent AI reviewers (J-P1 … J-P6), each with its own reading brief. They evaluate in isolated contexts and never see one another's scores.

**Dimension.** One of the six fixed questions every deck is scored on (P1 … P6). Dimensions are fixed so that every startup is compared against the same core questions — see [Dimensions P1–P6](./panel/dimensions.md).

**Routing weight.** How much a given judge's read counts toward a given dimension: primary 1.00, secondary 0.50, advisory 0.25, or not scored. A judge does not influence every dimension — see [The six judges](./panel/judges.md).

**Confidence.** A per-dimension signal of how well evidence supports the read. It is calculated separately and can apply a limited downward adjustment of at most 15%, so thin evidence does not produce a confident-looking number.

**Spread.** The highest judge score minus the lowest on one dimension. Under 1.5 is consensus, 1.5 to 2.99 is a split, 3.0 or more is a conflict. Spread never changes a score — it routes attention. See [Disagreement and spread](./scoring/disagreement-and-spread.md).

## The three scores

This is the distinction to get right before anyone presents a result.

| Score | Who produces it | What it does |
|---|---|---|
| **AI Criterion Score** | The panel, per dimension | The AI baseline for one dimension, with its evidence attached. Read-only. |
| **AI Total Score** | Deterministic aggregation, 0–10 | An advisory reference across all dimensions. It never ranks the batch. |
| **Jury Score** | A person, per dimension, 0.0–10.0 | The human scoring input. The leaderboard is built only from submitted Jury Scores. |

**Final Score** is what the leaderboard sorts on: your criterion weights applied to the Jury Score.

The rule that follows from the table: *if a ranking changed, a person changed it.* The AI Total Score can sit beside a Jury Score that disagrees with it, and the ranking will follow the human number.

## Evidence objects

**Finding.** A concrete signal that raised or lowered a dimension's score, pointing at the slide it came from — number, title and note — so the claim can be opened and checked.

**Deck completeness.** A check across ten core sections — Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask, Other — each marked present, thin or missing, with a severity of info, warning or critical, and the dimension it affects. Completeness is not a fact-check: *missing* means the deck did not cover it, not that a claim is false.

**Security signal.** A flag raised when the extraction stage detects an instruction aimed at the model inside a deck. The instruction is excluded from scoring evidence and surfaced to the organizer — see [Prompt-injection safety](./trust/prompt-injection-safety.md).

## The pipeline

Every deck passes the same five stages:

1. **Decoder** — PDF, PPTX or Google Slides becomes one structured, slide-level format.
2. **AI Judges** — the panel scores the deck across the dimensions, in parallel and in isolation.
3. **Summarizer** — deterministic math first, then the narrative and the questions to ask each team.
4. **Scoring** — your criterion weights apply to the human Jury Score to form the Final Score.
5. **Report** — an explainable report is assembled per participant.

## Next steps

- [How the score is built](./scoring/how-the-score-is-built.md) — the arithmetic behind the advisory number.
- [Read a report](./guides/read-a-report.md) — where each of these objects shows up on screen.
- [Glossary](./glossary.md) — the same terms in one alphabetical list.
