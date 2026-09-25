---
title: "How EvalLens scoring works: judges, dimensions and the advisory score"
description: "The scoring method in five pages: the six AI judges and their routing, the dimensions P1–P6, how the AI Total Score is built, what disagreement and spread mean, and what is reproducible."
status: generated
version: "0.1"
---

# Scoring method

An independent AI panel reads every submission against six fixed dimensions. A deterministic calculation combines those reads into an advisory AI Total Score.

**The leaderboard uses Jury Scores set by people.** The AI Total Score sits beside them for reference.

<!-- widget:cards plain cols=2 -->

## What goes in

- [The six judges](./judges.md) — Judge lenses, context isolation and the routing matrix {scan-eye}
- [Dimensions P1–P6](./dimensions.md) — The six questions, their anchors and red flags {list-checks}

## How it is calculated

- [How the score is built](./how-the-score-is-built.md) — Routing weights, confidence and aggregation {sigma}
- [Disagreement and spread](./disagreement-and-spread.md) — Consensus, split and conflict, and what each requires {git-compare}
- [Reproducibility](./reproducibility.md) — What is deterministic and what is benchmarked {repeat}

<!-- /widget -->

To change the weights for your round, see [Criteria and weights](../guides/criteria-and-weights.md).
