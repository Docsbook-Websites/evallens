---
title: "Disagreement and spread in EvalLens: consensus, split, conflict"
description: "Spread is the highest judge score minus the lowest on a dimension. Under 1.5 is consensus, 1.5–2.99 a split, 3.0 or more a conflict routed to human review. It never changes the score."
---

# Disagreement and spread

Two decks can have the same average score. One may have broad agreement; the other may split the judges. The average alone does not show the difference — and the case it hides is precisely the one a jury exists to discuss.

## The definition

**Spread** on a dimension is the highest judge score minus the lowest, across the reads that cover it.

| Spread | Label | What it means | What to do |
|---|---|---|---|
| < 1.5 | **Consensus** | The dimension reads the same way across the jury | Nothing. Trust the number as far as its evidence goes |
| 1.5 – 2.99 | **Split** | Judges diverge | Worth checking where the views split |
| ≥ 3.0 | **Conflict** | Strong disagreement | Flagged for human review — read both reads before scoring |

## What spread is not

**It is not a penalty.** A high spread does not lower a score automatically, and a low spread does not raise one. Spread routes attention; it does not participate in the arithmetic.

**It is not noise.** Judges score different dimensions with different routing weights and read the deck through different lenses. Disagreement between a Feasibility read and a Market read on the same dimension is information about the deck, not a malfunction of the panel.

## Reading spread together with the score

Four combinations, and each asks a different question:

| Pattern | What it usually means |
|---|---|
| High score · low spread | Strong, stable signal |
| High score · high spread | Strong score that needs review before you rely on it |
| Market strong · feasibility weak | An opportunity carrying execution risk |
| Low score · high spread | Contested, not simply weak — this one deserves the read |

The last row is the one worth pinning up. A contested low score and a agreed-upon low score look identical in a sorted list and mean very different things.

## Why this is published rather than smoothed

Averaging a conflict hides exactly the case a jury exists to discuss. Making disagreement visible has a second effect on human panels: judges who know disagreement is expected stop softening their scores toward the middle. That is why the spread rule belongs in the [briefing pack](../guides/brief-your-jury.md) as well as in the report.

## Using the rule without EvalLens

The rule works on paper. Per dimension, take the highest score minus the lowest across your human judges; under 1.5 is consensus, 1.5 to 2.99 is a split, and 3.0 or more goes to a conversation instead of an average. State the threshold and the resulting action in the pack before scoring starts, not after the leaderboard exists.

## Next steps

- [How the score is built](./how-the-score-is-built.md) — where spread sits in the pipeline (beside the arithmetic, not inside it).
- [Read a report](../guides/read-a-report.md) — where the flag appears and what the judge contribution matrix adds.
- [Reproducibility](./reproducibility.md) — run-to-run variance, which is a different question from judge-to-judge spread.
