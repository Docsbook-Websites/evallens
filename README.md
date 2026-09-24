---
title: "EvalLens documentation: run a selection round end to end"
description: "Documentation for EvalLens: configure a selection round, collect pitch decks, run the six-judge panel, inspect evidence, and set the human ranking."
status: generated
version: "0.2"
---

# EvalLens documentation

EvalLens is the evaluation layer for selection programs that receive more applications than their reviewers can read. Teams submit through one entry point, a panel of independent AI judges reads every submission against your rubric, and your jury receives an evidence-linked report. **The AI Total Score is advisory; the leaderboard is built from the Jury Score a person sets.**

This is the documentation entry point. Use the sections below to learn the vocabulary, run a round, inspect the scoring method, check the trust boundaries, or choose the material for your program type.

## Start with the workflow

<!-- widget:cards plain cols=2 -->

- [Getting started](./getting-started.md) — Create a project, collect a batch, run the panel, and generate a human-ranked leaderboard. {rocket}
- [Core concepts](./concepts.md) — Define projects, entries, judges, dimensions, scores, evidence, and the pipeline. {compass}
- [Run an evaluation](./guides/run-an-evaluation.md) — Follow Decoder, AI Judges, Summarizer, Scoring, and Report. {play}
- [Read a report](./guides/read-a-report.md) — Use the summary, evidence-linked score report, and questions for live Q&A. {file-text}

<!-- /widget -->

## Guides

<!-- widget:cards plain cols=2 -->

- [Set up a project](./guides/set-up-a-project.md) — Choose a mode, configure criteria and weights, add judges, and review the project. {settings}
- [Collect submissions](./guides/collect-submissions.md) — Add teams manually or collect decks through a public submission page. {inbox}
- [Criteria and weights](./guides/criteria-and-weights.md) — Review the default rubric, edit weights, and understand when they lock. {sliders}
- [Brief your jury](./guides/brief-your-jury.md) — Prepare the rubric, scoring procedure, disagreement rule, and calibration. {users}
- [Score and shortlist](./guides/score-and-shortlist.md) — Set Jury Scores, compare evidence, and generate the leaderboard. {gavel}
- [For applicants](./guides/for-applicants.md) — Explain what teams submit and what happens to their entry. {upload}

<!-- /widget -->

## Scoring and the panel

<!-- widget:cards plain cols=2 -->

- [The six judges](./panel/judges.md) — See what each independent lens reads and how routing works. {scan-eye}
- [Dimensions P1–P6](./panel/dimensions.md) — Review the six questions and their score anchors. {list-checks}
- [How the score is built](./scoring/how-the-score-is-built.md) — Trace routing weights, confidence, aggregation, and the Final Score. {calculator}
- [Disagreement and spread](./scoring/disagreement-and-spread.md) — Interpret consensus, split, and conflict signals. {git-compare}
- [Reproducibility](./scoring/reproducibility.md) — Separate deterministic aggregation from the model-based judge layer. {repeat}

<!-- /widget -->

## Trust and boundaries

<!-- widget:cards plain cols=2 -->

- [What EvalLens does not do](./trust/boundaries.md) — Understand the limits: no external truth check, investment advice, or automatic winner selection. {shield-alert}
- [Prompt-injection safety](./trust/prompt-injection-safety.md) — Treat a deck as evidence, never as an instruction to the evaluator. {shield}
- [Security and privacy](./trust/security-and-privacy.md) — See workspace scope, access control, and report delivery. {lock}

<!-- /widget -->

## By program type

<!-- widget:cards plain cols=2 -->

- [Pitch competitions](./use-cases/pitch-competitions.md) — Apply the workflow to a written-round or pitch-competition field. {trophy}
- [Accelerators](./use-cases/accelerators.md) — Apply one standard across a cohort while keeping committee decisions human. {rocket}
- [VC open calls](./use-cases/vc-open-calls.md) — Turn inbound decks into a partner-ready first read. {briefcase}
- [Grants and prizes](./use-cases/grants-and-prizes.md) — Keep a score and evidence trail that can survive an appeal. {award}
- [Hackathons](./use-cases/hackathons.md) — Use execution-weighted judging before the expo floor. {wrench}

<!-- /widget -->

## Reference pages

- [FAQ](./faq.md) — Answers to recurring organizer questions.
- [Glossary](./glossary.md) — Alphabetical definitions for the terms used across the docs.
- [Pricing](./pricing.md) — Packages, submission counts, validity windows, and what each package includes.

The documentation keeps the distinction between preparation and decision explicit: AI judges read and explain the evidence, while people set the Jury Scores and make the final ranking.
