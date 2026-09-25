---
title: "EvalLens reproducibility: what is deterministic and what is measured"
description: "Aggregation is deterministic; the judge layer is benchmarked. The published repeatability numbers, the benchmark scope, the targets for the controlled set, and what is still in progress."
status: generated
version: "0.1"
---

# Reproducibility

"Same deck, same score" is two claims in EvalLens, held to two standards. Merging them is how a reliability claim quietly becomes untrue.

## Layer 1 · Aggregation is deterministic

Once judge outputs exist, a deterministic function calculates the score — **not another model call**. The same outputs and weights give the same AI Total Score every time, within rounding.

This is a property of the code path, not a statistic. It is why "how did this number come about" always has an answer, and why re-ranking under new weights needs no re-run.

## Layer 2 · The judge layer is measured

The judge layer runs on a language model, so repeated runs can differ. Its repeatability is benchmarked and published rather than assumed.

| Measure | Result |
|---|---|
| Score standard deviation across 24 reruns of the same deck | **0.096** |
| Run-to-run variance after the latest calibration prompt, against the prior prompt | **~60% lower** |
| Reruns that reproduced the same dimension profile | **~86%** (12 of 14) |
| Aggregation consistency check (same inputs → same total) | **<1%** deviation |

<!-- widget:callout type=info -->

**Benchmark scope.** Internal repeatability benchmark: J-P5 Team Readiness, one deck, 24 runs, June 2026. A multi-deck regression across the full panel is in progress. A single-deck, single-lens result is evidence about that lens on that deck, not about every deck type.

<!-- /widget -->

## Targets for the controlled set

Published as targets, which is a different thing from a result:

- Final-score standard deviation ≤ 3
- Score-band consistency ≥ 90%
- Critical-risk recall ≥ 90%
- Schema-valid outputs ≥ 99%
- Regression pass ≥ 95%

## Method origin: 1,000+ internal runs

EvalLens comes out of 1,000+ internal evaluation runs, starting with an Amazon Nova hackathon prototype and the earlier AI Jury system. The current method — fixed dimensions, independent lenses, deterministic aggregation — has 400+ runs behind it.

Adding more judges was tried and did not help: scores shifted, roles overlapped, and long reports added noise. Structure changed the outcome, not headcount.

## Limits: reproducibility is not accuracy

Reproducibility is not accuracy. EvalLens does not predict startup success, and calibration across every deck type is still being proven. The numbers above support something narrower: the same deck read twice lands in the same place often enough that a score is a signal, not a coin flip, and the arithmetic on top does not move at all.

That is also why the final call stays human. See [What EvalLens does not do](../trust/boundaries.md).

## Reproducibility versus spread

Two different questions that both look like "the judges disagreed":

- **Reproducibility** — would the *same* lens produce the same read on a rerun? Measured above.
- **Spread** — do *different* lenses agree with each other on this deck? A per-deck signal, covered in [Disagreement and spread](./disagreement-and-spread.md).

A deck can be perfectly reproducible and heavily contested. That combination is a real finding about the deck.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Score calculation](./how-the-score-is-built.md) — The deterministic path in detail {sigma}
- [What EvalLens does not do](../trust/boundaries.md) — The four boundaries, stated plainly {shield-alert}
- [Prompt-injection safety](../trust/prompt-injection-safety.md) — The other published test and its scope {shield-check}

<!-- /widget -->
