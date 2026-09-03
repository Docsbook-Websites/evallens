---
title: "EvalLens documentation: run a selection round end to end"
description: "How EvalLens collects pitch decks, reads every one against your rubric with a six-judge AI panel, and hands your jury an evidence-linked report. The human sets the score."
---

# EvalLens documentation

EvalLens is the evaluation layer for selection programs that receive more applications than their reviewers can read. Teams submit through one entry point, a panel of independent AI judges reads every submission against your rubric, and your jury gets an evidence-linked report and a ranked board. **The AI Total Score is advisory; the leaderboard is built from the Jury Score a person sets.**

These pages document how that works in practice: what to configure before a run, what happens to a deck inside the pipeline, how to read what comes back, and what EvalLens deliberately does not do.

<!-- widget:cards -->

## Start here

- [Getting started](./getting-started.md) — from the partner call to your first ranked leaderboard {rocket}
- [Core concepts](./concepts.md) — project, entry, judge, dimension, and the three different scores {compass}
- [Pricing](./pricing.md) — what a package includes and how submissions are counted {credit-card}
- [FAQ](./faq.md) — the questions organizers ask before the first batch {circle-help}

## Run a round

- [Set up a project](./guides/set-up-a-project.md) — the five-step wizard: details, criteria, judges, intake, review {settings}
- [Collect submissions](./guides/collect-submissions.md) — manual entry or a public submission page {inbox}
- [Run an evaluation](./guides/run-an-evaluation.md) — readiness checks and the five pipeline stages {play}
- [Read a report](./guides/read-a-report.md) — the three layers and what each one is for {file-text}
- [Score and shortlist](./guides/score-and-shortlist.md) — Review Board, Jury Scores, leaderboard {gavel}
- [Criteria and weights](./guides/criteria-and-weights.md) — the default rubric, editing it, and the lock {sliders}
- [Brief your jury](./guides/brief-your-jury.md) — the six-block briefing pack and the 11-minute calibration {users}
- [For applicants](./guides/for-applicants.md) — what teams submit and what happens to it {upload}

## The panel

- [The six judges](./panel/judges.md) — what each lens reads and why they never see each other {scan-eye}
- [Dimensions P1–P6](./panel/dimensions.md) — the six questions, with anchors for a 3 against a 7 {list-checks}

## Scoring

- [How the score is built](./scoring/how-the-score-is-built.md) — routing weights, confidence, aggregation {calculator}
- [Disagreement and spread](./scoring/disagreement-and-spread.md) — consensus, split, conflict {git-compare}
- [Reproducibility](./scoring/reproducibility.md) — what is deterministic, what is measured {repeat}

## Trust

- [What EvalLens does not do](./trust/boundaries.md) — the four things it is not {shield-alert}
- [Prompt-injection safety](./trust/prompt-injection-safety.md) — a deck is evidence, never an instruction {shield}
- [Security and privacy](./trust/security-and-privacy.md) — workspace scope, access control, report delivery {lock}

## By program type

- [Pitch competitions](./use-cases/pitch-competitions.md) — the written round, pre-read {trophy}
- [Accelerators](./use-cases/accelerators.md) — one standard across a cohort {rocket}
- [VC open calls](./use-cases/vc-open-calls.md) — inbound decks into a partner-ready first read {briefcase}
- [Grants and prizes](./use-cases/grants-and-prizes.md) — a score that survives an appeal {award}
- [Hackathons](./use-cases/hackathons.md) — execution-weighted judging before the expo floor {wrench}

<!-- /widget -->

## What makes an EvalLens score different

**Evidence comes before the number.** A judge must cite the slide, state what supports the score and what lowers it, name the rubric band, and only then pick a number inside that band. On a boundary with evidence missing, the rule is the lower band.

**Six lenses, not one opinion.** Six judges read each deck independently and never see one another's scores. Where they disagree, the report shows the spread instead of averaging it away.

**The arithmetic is deterministic.** No model call runs during final aggregation: the same judge outputs and weights produce the same AI Total Score every time.

**The ranking is human.** The leaderboard is built only from submitted Jury Scores and your criterion weights. The AI Total Score sits beside them as a read-only reference.

## Where this fits

EvalLens does not replace your judges, your intake tool, or your rules. It runs the first read of the whole field so that judge hours go to decisions instead of triage — and leaves a record that explains, months later, why a submission placed where it did.

<!-- widget:cta -->

**Run it on your own field**

## Book a partner call

EvalLens is currently available through a limited partner program: there is no public sign-up. Tell us what your program reviews and roughly how many decks are in the pile, and access is set up for your team.

[Book a call](https://calendly.com/evallens/30min) · [Getting started](./getting-started.md)

<!-- /widget -->
