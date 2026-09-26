---
title: "Sources and scope"
description: "Sources behind the EvalLens pitch-evaluation methodology, and the boundary between documented method and external research."
status: generated
version: "0.1"
---

# Sources and scope

This page separates the sources used to describe the pitch-evaluation methodology from the method implemented in EvalLens. The methodology combines a fixed rubric, evidence-grounded review, independent judge lenses, deterministic score aggregation and human-controlled ranking.

## Primary sources

These are the authoritative sources for the terminology and mechanics described in this documentation.

- [EvalLens methodology](https://www.evallens.io/trust/methodology) — Public overview of the method, its foundations, the P1–P6 dimension matrix, evidence-first scoring and the human decision boundary.
- [EvalLens product overview](https://www.evallens.io/product/overview) — Product description of the evaluation pipeline, six judge lenses, reports and human review.
- [Dimensions P1–P6](./scoring/dimensions.md) — The six questions, default weights, score anchors and evidence-first procedure used in the documentation.
- [Score calculation](./scoring/how-the-score-is-built.md) — Routing weights, confidence adjustment, aggregation and the distinction between the advisory AI Total Score and the human Final Score.
- [Score and shortlist](./guides/score-and-shortlist.md) — Operational procedure for reviewing evidence, entering Jury Scores and generating the leaderboard.

## Methodological foundations named by EvalLens

The public methodology page describes three foundations for the Pitch Competition dimension matrix:

- **Lean Startup** — hypothesis and problem–solution logic; reflected primarily in P1 and P2.
- **Customer Development** — customer, pain and validation evidence; reflected primarily in P1 and P2.
- **VC due diligence** — market, business model, team and feasibility analysis; reflected primarily in P3, P4, P5 and P6.

These labels describe the conceptual foundations named by EvalLens. They are not presented here as a citation to a particular book, paper or investment firm's proprietary framework.

## What this documentation does not claim

The rubric is a decision-support method, not a prediction model or an investment recommendation. EvalLens evaluates what is present in a pitch deck, records missing evidence and prepares a comparable review; it does not verify every claim against the outside world, provide investment advice or select a winner automatically.

The AI Total Score is advisory. The final ranking is produced from human Jury Scores and project weights, as described in [Score calculation](./scoring/how-the-score-is-built.md).

## External research status

This page currently cites the product's public methodology and the maintained documentation. A separate bibliography of external academic, accelerator or investment sources should be added only after each source has been verified and its relevance to a specific criterion is documented. No unverified external citation is included here.

## Related pages

- [Scoring method](./scoring/README.md) — The complete scoring reference.
- [Trust and safety](./trust/README.md) — Boundaries, security and prompt-injection handling.
- [Glossary](./glossary.md) — Terms used throughout the documentation.
