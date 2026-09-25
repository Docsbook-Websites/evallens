---
title: "EvalLens score calculation: routing, confidence and aggregation"
description: "From six judge reads to one advisory AI Total Score — routing weights per dimension, the 15% confidence adjustment, deterministic aggregation, and where your weights apply."
---

# Score calculation

A fixed calculation combines judge outputs into an advisory AI Total Score on a 0–10 scale. This page is the arithmetic, in the order it runs.

## 1 · Per-dimension: the criterion score

For each dimension, the judge scores that cover it become a weighted average by **routing weight**: primary 1.00, secondary 0.50, advisory 0.25. Inputs: judge score, routing weight, confidence.

Which judge covers which dimension: [the routing matrix](./judges.md).

## 2 · Confidence adjustment

Confidence is calculated separately and can move a score **down by at most 15%**, never up. A well-argued read of a deck that lacks the evidence should not present as a firm number.

## 3 · Across dimensions: the AI Total Score

Project weights combine the AI Criterion Scores into one advisory AI Total Score on a 0–10 scale. It informs human review; **it does not determine the ranking.**

## 4 · Review signal: spread

Spread flags consensus, split or conflict between primary and secondary judges on a dimension. It is computed alongside the score and **does not change it** — it tells reviewers where to look closer. See [Disagreement and spread](./disagreement-and-spread.md).

## 5 · Final Score from human Jury Scores

Your criterion weights are applied to the **human Jury Score** to produce the Final Score, and the leaderboard is ranked on that. The AI Total Score sits beside it as a read-only reference.

Because weights apply at this stage rather than inside each judge's reading, the same evidence can be re-ranked under different weights without re-running the batch.

## Deterministic aggregation: no model call

**No model call runs during final aggregation.** Once judge outputs exist, the combination is arithmetic: the same judge scores, routing weights, confidence values and criterion weights give the same result every time.

<!-- widget:callout type=note -->

This covers the aggregation layer only. The judge layer runs on a language model and is measured, not assumed — see [Reproducibility](./reproducibility.md).

<!-- /widget -->

## Reading the whole chain

| Stage | Produced by | Changes the ranking? |
|---|---|---|
| Judge score per dimension | One AI lens, with cited evidence | No |
| AI Criterion Score | Routing-weighted combination + confidence | No |
| AI Total Score | Project weights across dimensions | No |
| Spread | Highest minus lowest judge score | No |
| **Jury Score** | **A person, per dimension** | **Yes** |
| Final Score | Your weights × Jury Score | Yes — this is the ranking |

Everything above the bold line is preparation. The ranking has exactly one input, and a human supplies it.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Disagreement and spread](./disagreement-and-spread.md) — The thresholds and what each asks of you {git-compare}
- [Reproducibility](./reproducibility.md) — What has been benchmarked {repeat}
- [Score and shortlist](../guides/score-and-shortlist.md) — Where the Jury Score is entered {gavel}

<!-- /widget -->
