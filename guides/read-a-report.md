---
title: "Read an EvalLens report"
description: "Use the Project Summary, AI Score Report, evidence links, completeness signals and live questions to prepare a human review."
status: generated
version: "0.2"
---

# Read an EvalLens report

Read the three report layers in order: what the project is, the evidence behind the scores, then the live questions.

## Project Summary

Start here for the fast read: what the project does, how it scored, its strengths and risks, and what to verify with the team.

## AI Score Report

Use these sections to explain a number:

- **Per-dimension breakdown** — score, confidence, supporting and limiting evidence, and what could change the read.
- **Judge contribution matrix** — which lenses contributed and at what level.
- **Score formation** — dimension score, weight and contribution.
- **Methodology** — the scale and scoring rules applied to the batch.
- **Initial criteria** — the project weights used for every team.
- **Judge conclusions** — each judge's main takeaway, concern and live question.

The AI Total Score is context, not the human decision.

## Questions for live Q&A

Questions are ranked by priority and linked to the dimension they test. Use them to probe gaps rather than replay the deck.

## Verify a finding

Every finding points to the slide that supports it. Check it in this order:

1. Open the cited slide.
2. Check what supports the score.
3. Check what lowers it or stays unproven.
4. Compare the evidence with the named rubric band in [Dimensions P1–P6](../scoring/dimensions.md).
5. Record the question your jury still needs answered.

## Interpret completeness correctly

The report checks ten sections: Problem, Solution, Market, Business Model, Traction, Team, Roadmap, Financials, Ask and Other.

<!-- widget:callout type=warning -->

`missing` means the deck did not cover a section. It does not mean a claim is false: EvalLens is not an external fact-check. See [What EvalLens does not do](../trust/boundaries.md).

<!-- /widget -->

## Read confidence and spread together

- **Confidence** — how well the evidence supports the read. A low-confidence read can be adjusted down by at most `15%`.
- **Spread** — highest judge score minus lowest. Under `1.5` is consensus, `1.5–2.99` a split, `3.0` or more a conflict.

A high score with high spread is a prompt for discussion, not an automatic rejection.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Score and shortlist](./score-and-shortlist.md) — Turn reports into a human ranking {gavel}
- [Dimensions P1–P6](../scoring/dimensions.md) — Compare a 3 with a 7 {list-checks}
- [Score calculation](../scoring/how-the-score-is-built.md) — Follow the arithmetic {sigma}

<!-- /widget -->
