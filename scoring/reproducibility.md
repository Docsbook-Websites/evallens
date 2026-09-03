---
title: "EvalLens reproducibility: what is deterministic and what is measured"
description: "Aggregation is deterministic; the judge layer is benchmarked. The published repeatability numbers, the benchmark scope, the targets for the controlled set, and what is still in progress."
---

# Reproducibility

"Same deck, same score" is two separate claims in EvalLens, and they are held to two different standards. Conflating them is how a reliability claim quietly becomes untrue.

## Layer 1 · Aggregation is deterministic

Once judge outputs exist, the score is calculated by a deterministic aggregation function — **not another model call**. The same judge outputs and weights produce the same AI Total Score every time, with only rounding-level tolerance.

This is a property of the code path, not a statistical result. It is why "how did this number come about" always has an answer, and why re-ranking the same evidence under different weights does not require re-running anything.

## Layer 2 · The judge layer is measured

The AI judge layer runs on a language model, so repeated runs are not always identical. Rather than assume stability, that repeatability is benchmarked and the results published.

| Measure | Result |
|---|---|
| Score standard deviation across 24 reruns of the same deck | **0.096** |
| Run-to-run variance after the latest calibration prompt, against the prior prompt | **~60% lower** |
| Reruns that reproduced the same dimension profile | **~86%** (12 of 14) |
| Aggregation consistency check (same inputs → same total) | **<1%** deviation |

**Benchmark scope.** Internal repeatability benchmark: J-P5 Team Readiness, one deck, 24 runs, June 2026. A multi-deck regression across the full panel is in progress. The scope is stated because a single-deck, single-lens result is evidence about that lens on that deck — not a claim about every deck type.

## The targets for the controlled set

Published as targets, which is a different thing from a result:

- Final-score standard deviation ≤ 3
- Score-band consistency ≥ 90%
- Critical-risk recall ≥ 90%
- Schema-valid outputs ≥ 99%
- Regression pass ≥ 95%

## Where the method came from

EvalLens comes out of 1,000+ internal evaluation runs, starting with an Amazon Nova hackathon prototype and the earlier AI Jury system. The current method — fixed dimensions, independent lenses, deterministic aggregation — has 400+ runs behind it. Adding more judges was tried and did not solve quality: scores shifted, roles overlapped, and long reports produced noise instead of clarity. What changed the outcome was structure, not headcount.

## The honest edge

Reproducibility is not accuracy. EvalLens does not promise to predict startup success, and absolute calibration across every deck type is still being proven. What the numbers above support is narrower and more useful: the same deck read twice lands in the same place often enough that a score is a signal rather than a coin flip, and the arithmetic on top of it does not move at all.

That is also why the final call stays human. See [What EvalLens does not do](../trust/boundaries.md).

## Reproducibility versus spread

Two different questions that both look like "the judges disagreed":

- **Reproducibility** — would the *same* lens produce the same read on a rerun? Measured above.
- **Spread** — do *different* lenses agree with each other on this deck? A per-deck signal, covered in [Disagreement and spread](./disagreement-and-spread.md).

A deck can be perfectly reproducible and heavily contested. That combination is a real finding about the deck.

## Next steps

- [How the score is built](./how-the-score-is-built.md) — the deterministic path in detail.
- [What EvalLens does not do](../trust/boundaries.md) — the four boundaries, stated plainly.
- [Prompt-injection safety](../trust/prompt-injection-safety.md) — the other published test, with its own scope statement.
