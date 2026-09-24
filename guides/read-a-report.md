---
title: "Read an EvalLens report"
description: "Use the Project Summary, AI Score Report, evidence links, completeness signals and live questions to prepare a human review."
status: generated
version: "0.2"
---

# Read an EvalLens report

Read the three report layers in order: identify the project, inspect the evidence behind the scores, then prepare the live questions.

## Project Summary

Start here for the fast read: what the project does, how it scored, strengths, risks and what to verify with the team.

## AI Score Report

Use these sections to explain a number:

- **Per-dimension breakdown** — score, confidence, supporting evidence, limiting evidence and what could change the read.
- **Judge contribution matrix** — which lenses contributed and at what level.
- **Score formation** — dimension score, weight and contribution.
- **Methodology** — the scale and scoring rules applied to the batch.
- **Initial criteria** — the project weights used for every team.
- **Judge conclusions** — the main takeaway, concern and live question from each judge.

The AI Total Score is context. It is not the human decision.

## Questions for live Q&A

Questions are ranked by priority and linked to the dimension they test. Use them to investigate gaps rather than repeat the deck.

## Verify a finding

Every finding should point to the slide that supports it. Read the evidence in this order:

1. Open the cited slide.
2. Check what supports the score.
3. Check what lowers the score or remains unproven.
4. Compare the evidence with the named rubric band.
5. Record the question your jury still needs answered.

## Interpret completeness correctly

The report checks ten sections: Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask and Other.

`missing` means the deck did not cover a section. It does not mean the claim is false. EvalLens is not an external fact-check; see [What EvalLens does not do](../trust/boundaries.md).

## Read confidence and spread together

- **Confidence** describes how well the evidence supports the read. A low-confidence read can receive a downward adjustment of at most `15%`.
- **Spread** is the difference between the highest and lowest judge score. Under `1.5` is consensus, `1.5–2.99` is a split, and `3.0` or more is a conflict.

A high score with high spread is a prompt for discussion, not an automatic rejection.

## Next steps

- [Score and shortlist](./score-and-shortlist.md) — turn reports into a human ranking.
- [Dimensions P1–P6](../panel/dimensions.md) — compare a 3 with a 7.
- [How the score is built](../scoring/how-the-score-is-built.md) — follow the arithmetic.
