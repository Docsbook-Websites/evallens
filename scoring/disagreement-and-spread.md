---
title: "Disagreement and spread in EvalLens: consensus, split, conflict"
description: "Spread is the highest judge score minus the lowest on a dimension. Under 1.5 is consensus, 1.5–2.99 a split, 3.0 or more a conflict routed to human review. It never changes the score."
status: generated
version: "0.1"
---

# Disagreement and spread

Two decks can share an average score while one has broad agreement and the other splits the judges. The average hides the difference, and the split case is the one a jury exists to discuss.

## Spread: the definition

**Spread** on a dimension is the highest judge score minus the lowest, across the reads that cover it.

| Spread | Label | What it means | What to do |
|---|---|---|---|
| < 1.5 | **Consensus** | The dimension reads the same way across the jury | Nothing. Trust the number as far as its evidence goes |
| 1.5 – 2.99 | **Split** | Judges diverge | Worth checking where the views split |
| ≥ 3.0 | **Conflict** | Strong disagreement | Flagged for human review — read both reads before scoring |

## Misreadings of spread

- **It is not a penalty.** High spread does not lower a score, and low spread does not raise one. Spread routes attention; it stays out of the arithmetic.
- **It is not noise.** Judges read the deck through different lenses with different routing weights. A Feasibility read and a Market read disagreeing on one dimension is information about the deck, not a panel fault.

## Reading spread together with the score

Four combinations, and each asks a different question:

| Pattern | What it usually means |
|---|---|
| High score · low spread | Strong, stable signal |
| High score · high spread | Strong score that needs review before you rely on it |
| Market strong · feasibility weak | An opportunity carrying execution risk |
| Low score · high spread | Contested, not simply weak — this one deserves the read |

<!-- widget:callout type=tip -->

**Pin up the last row.** A contested low score and an agreed low score look identical in a sorted list and mean very different things.

<!-- /widget -->

## Published, not smoothed: why conflicts stay visible

Averaging a conflict hides the case a jury exists to discuss. Visible disagreement also changes human panels: judges who expect it stop softening scores toward the middle. That is why the spread rule belongs in the [briefing pack](../guides/brief-your-jury.md) as well as the report.

## Using the rule without EvalLens

The rule works on paper. Per dimension, take your human judges' highest score minus the lowest: under 1.5 is consensus, 1.5 to 2.99 a split, 3.0 or more goes to a conversation instead of an average. State the threshold and the action in the pack before scoring starts.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Score calculation](./how-the-score-is-built.md) — Where spread sits: beside the arithmetic {sigma}
- [Read a report](../guides/read-a-report.md) — Where the flag appears in a report {file-text}
- [Reproducibility](./reproducibility.md) — Run-to-run variance, a different question {repeat}

<!-- /widget -->
