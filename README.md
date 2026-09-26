---
title: "EvalLens documentation"
description: "Practical reference for setting up a selection project, collecting submissions, running an AI-assisted evaluation, and making the final human ranking."
status: generated
version: "0.7"
---

# EvalLens documentation

EvalLens helps a review team read a large field consistently. You collect submissions, an independent AI panel reads them against your rubric, and people set the scores that rank them.

<!-- widget:callout type=info -->

**The AI Total Score is advisory.** The leaderboard uses [Jury Scores](./concepts.md) set by people.

<!-- /widget -->

## Documentation sections

Each section opens on an overview of its pages.

<!-- widget:cards feature cols=2 -->

- [Guides](./guides/README.md) — Run a selection round task by task, from setup to shortlist. {book-open} {color:green}
- [Scoring method](./scoring/README.md) — Judges, dimensions P1–P6, the score arithmetic and its reproducibility. {calculator} {color:purple}
- [Trust and safety](./trust/README.md) — What EvalLens does not do, prompt injection, and who can read a deck. {shield} {color:blue}
- [Use cases](./use-cases/README.md) — How hackathons, competitions, accelerators, grants and VC calls run a round. {trophy} {color:amber}

<!-- /widget -->

## Selection round in three stages

Pick the stage you are in. [Getting started](./getting-started.md) walks all three on one page.

<!-- widget:journey -->

### Prepare the round

- [Set up a project](./guides/set-up-a-project.md) {settings}
- [Criteria and weights](./guides/criteria-and-weights.md) {sliders-horizontal}
- [Brief your jury](./guides/brief-your-jury.md) {users}
- [Collect submissions](./guides/collect-submissions.md) {inbox}

### Run the panel

- [Run an evaluation](./guides/run-an-evaluation.md) {play}
- [Read a report](./guides/read-a-report.md) {file-text}
- [Disagreement and spread](./scoring/disagreement-and-spread.md) {git-compare}

### Decide

- [Score and shortlist](./guides/score-and-shortlist.md) {gavel}
- [What EvalLens does not do](./trust/boundaries.md) {shield-alert}
- [For applicants](./guides/for-applicants.md) {send}

<!-- /widget -->

## Find your program

<!-- widget:cards plain cols=3 arrow=hover -->

- [Hackathons](./use-cases/hackathons.md) — Execution-weighted judging {code}
- [Pitch competitions](./use-cases/pitch-competitions.md) — The written round pre-read {presentation}
- [Accelerators](./use-cases/accelerators.md) — Cohort intake at volume {sprout}
- [Grants and prizes](./use-cases/grants-and-prizes.md) — A locked rubric and an appeal file {hand-coins}
- [VC open calls](./use-cases/vc-open-calls.md) — Every deck read against your dimensions {briefcase}

<!-- /widget -->

## Reference pages

<!-- widget:cards plain cols=3 arrow=hover -->

### Terms and scoring

- [Core concepts](./concepts.md) — Projects, entries, scores and pipeline terms {compass}
- [AI judges](./scoring/judges.md) — Judge lenses and routing weights {scan-eye}
- [Dimensions P1–P6](./scoring/dimensions.md) — Questions and scoring anchors {list-checks}
- [Score calculation](./scoring/how-the-score-is-built.md) — Aggregation and weighting {sigma}
- [Reproducibility](./scoring/reproducibility.md) — What is deterministic and what is measured {repeat}

### Safety, pricing and answers

- [Prompt-injection safety](./trust/prompt-injection-safety.md) — Deck text is evidence, never an instruction {shield-check}
- [Security and privacy](./trust/security-and-privacy.md) — Access and report handling {lock}
- [Pricing](./pricing.md) — Packages, submission counting and validity {credit-card}
- [FAQ](./faq.md) — Operational questions {circle-help}
- [Glossary](./glossary.md) — Every term in one list {book-a}
- [Sources and scope](./sources.md) — Method sources, foundations and citation boundaries {library}

<!-- /widget -->

## Decision rule: people rank, the panel prepares

EvalLens prepares a comparable first read. It does not verify claims, give investment advice or choose a winner.

Your team reviews the evidence, sets Jury Scores and keeps the decision trail.
