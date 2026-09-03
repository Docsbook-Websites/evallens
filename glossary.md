---
title: "EvalLens glossary"
description: "Every EvalLens term in one list: advisory score, AI judge panel, batch, confidence, deck triage, deterministic aggregation, entry, Final Score, Jury Score, routing weight, spread."
---

# Glossary

**Advisory score.** A score that informs a decision without making it. In EvalLens the AI Total Score is advisory: it appears beside the human score and never orders the leaderboard.

**AI Criterion Score.** The AI baseline for one dimension, produced by combining the judge reads that cover it with their routing weights. Read-only.

**AI judge panel.** The set of independent AI reviewers that read every submission. Six lenses in Pitch Competition mode, five in Hackathon mode. They never see one another's scores.

**AI Total Score.** The advisory 0–10 number across all dimensions, produced by deterministic aggregation. It never ranks the batch.

**Anchor.** The description of what a given band looks like on a given dimension — what a 3 looks like against a 7. Anchors are what turn a ten-point scale into a scale judges use the same way.

**Band.** A range on the scoring scale (0–3, 4–6, 7–8, 9–10) with its own anchor description. A judge names the band before picking a number inside it.

**Batch.** All entries in a project, evaluated in one run rather than deck by deck.

**Confidence.** A per-dimension signal of how well the evidence supports a read. It can apply a downward adjustment of at most 15%, and never an upward one.

**Deck completeness.** A check across ten core sections — Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask, Other — marking each present, thin or missing with a severity. Not a fact-check.

**Deck triage.** Screening a large field to decide what deserves a full human read. The job EvalLens's first read is built for.

**Deterministic aggregation.** Combining judge outputs into a score with fixed arithmetic and no model call, so the same inputs always produce the same total.

**Dimension.** One of the six fixed questions a deck is scored on (P1–P6).

**Entry.** One team's submission: the deck, the team and project details, an optional note for judges, and a status.

**Entry Hub.** The intake side of EvalLens — manual entry or a public submission page with access rules and a window.

**Evidence-grounded scoring.** Requiring a slide reference behind every claim a score relies on. No slide, no claim.

**Final Score.** Your criterion weights applied to the Jury Score. The number the leaderboard sorts on.

**Judge contribution matrix.** The report view showing which judges contributed to each dimension and where strong disagreements were flagged.

**Jury Score.** The human score, set per dimension from 0.0 to 10.0. The only input to the ranking.

**Leaderboard.** The ranked view of a batch, built from submitted Jury Scores and project weights.

**LLM-as-a-judge.** The general practice of using a language model to score outputs against criteria. EvalLens's version differs in three ways: several independent lenses rather than one verdict, evidence required before a number, and the arithmetic on top removed from the model entirely.

**Mode.** Chosen when a project is created; determines the panel and the rubric shape. Pitch Competition or Hackathon.

**Project.** One selection round, with its own criteria, weights, judges and intake settings.

**Review Board.** The decision workspace: the whole batch with statuses, scores, findings, comparison and the leaderboard.

**Routing weight.** How much a judge's read counts toward a dimension — primary 1.00, secondary 0.50, advisory 0.25, or not scored.

**Score spread.** Highest judge score minus lowest on a dimension. Under 1.5 consensus, 1.5–2.99 split, 3.0 or more conflict. It routes attention and never changes a score.

**Security signal.** A flag raised when an instruction aimed at the model is detected inside a deck. The instruction is excluded from scoring evidence and shown to the organizer.

**SourceRef.** The link from a finding back to the slide it came from — number, title and note.

**Submission (billing).** One deck that received one successfully generated evaluation report. Unprocessable decks do not count.

## Next steps

- [Core concepts](./concepts.md) — the same terms in the order they appear in a run.
- [How the score is built](./scoring/how-the-score-is-built.md) — where each of the score terms enters the arithmetic.
