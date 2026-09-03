---
title: "How the EvalLens score is built: routing, confidence and aggregation"
description: "From six judge reads to one advisory AI Total Score — routing weights per dimension, the 15% confidence adjustment, deterministic aggregation, and where your weights apply."
---

# How the score is built

A fixed calculation combines judge outputs into an advisory AI Total Score on a 0–10 scale. This page is the arithmetic, in the order it runs.

## 1 · Per-dimension: the criterion score

For each dimension, the judge scores that cover it are combined using their **routing weights** — primary 1.00, secondary 0.50, advisory 0.25 — into a weighted average. Primary judges carry the strongest influence; advisory judges add context without dominating.

The inputs at this stage are: judge score, routing weight, confidence.

Which judge covers which dimension: [the routing matrix](../panel/judges.md).

## 2 · The confidence adjustment

Confidence is calculated separately from the score and can apply a **limited downward adjustment, capped at 15%**.

It exists to reduce overconfidence when evidence is thin. It only moves a score down, never up — a well-argued read on a deck that simply does not contain the evidence should not present as a firm number.

## 3 · Across dimensions: the AI Total Score

Project weights combine the AI Criterion Scores into one advisory AI Total Score on a 0–10 scale.

This number informs human review. **It does not determine the final ranking.**

## 4 · The review signal: spread

Spread flags consensus, split or conflict between primary and secondary judges on a dimension. It is computed alongside the score and **does not change it** — it tells reviewers where to look closer. See [Disagreement and spread](./disagreement-and-spread.md).

## 5 · The Final Score

Your criterion weights are applied to the **human Jury Score** to produce the Final Score, and the leaderboard is ranked on that. The AI Total Score sits beside it as a read-only reference.

Because weights apply at this stage rather than inside each judge's reading, the same evidence can be re-ranked under different weights without re-running the batch.

## What is deterministic

**No model call runs during final aggregation.** Once judge outputs exist, the combination is arithmetic: the same judge scores, routing weights, confidence values and criterion weights produce the same result every time.

That is a stronger claim than "the tool is consistent", and a narrower one. It applies to the aggregation layer only. The judge layer runs on a language model and is measured rather than assumed — the published repeatability numbers are on [Reproducibility](./reproducibility.md).

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

- [Disagreement and spread](./disagreement-and-spread.md) — the thresholds and what each one asks you to do.
- [Reproducibility](./reproducibility.md) — what has been benchmarked, and what has not.
- [Score and shortlist](../guides/score-and-shortlist.md) — where the Jury Score is entered.
