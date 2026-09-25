---
title: "Running a hackathon with EvalLens: execution-weighted judging"
description: "Five reviewer roles, a rubric where Execution and Demo carries 0.30 and Technical Depth 0.20, judges briefed before the expo floor opens, and the record for the Monday Discord thread."
---

# Hackathons

Hackathon judging software — sometimes called hackathon management software — collects submissions, scores every project against a published rubric, and gives each judge a structured read before the table visit, so a result survives being questioned in public. EvalLens runs that layer for hackathons: a five-role AI panel pre-reads every submission against a weighted rubric, briefs each judge with cited evidence, and keeps the record organizers show a team that asks "how was this scored?"

At a hackathon the rubric puts most of the weight on execution and innovation, and then asks a judge to grade both from a three-minute demo video and a four-minute table visit. That gap is what a first read closes.

## Judging table, honestly

| Figure | What it is |
|---|---|
| 4 min | All the time the MLH organizer guide budgets per project per judge: 2 minutes of demo, 1 for questions and scoring, 1 to walk to the next table |
| 18 judges | What the MLH formula J = ceil(P × n × t / T) demands for 175 projects in a two-hour expo at three rounds each |
| ~5% | Share of projects the average judge actually saw at HackMIT, where 100 judges covered more than 200 projects |
| 70% | Share of a standard Devpost rubric riding on technical execution and innovation, assessed from a demo video nobody is required to watch to the end |

## Hackathon panel: five reviewer roles

Hackathon mode runs **five reviewer roles** — Innovation, Technical Execution, Business Value, Pitch Quality and Feasibility — reading every submission independently across six dimensions.

The rubric changes shape rather than just weight:

| Dimension | Weight |
|---|---|
| Execution and Demo | **0.30** (weight-protected) |
| Technical Depth | **0.20** (weight-protected) |
| Problem Impact | 0.15 |
| Innovation / Divergence | 0.15 |
| UX Clarity | 0.10 |
| Delivery Readiness | 0.10 |

Execution and technical depth are protected precisely so that **a polished story cannot outrank a working build**. Weights are yours to set before the run and lock when it starts.

## Six steps to run a hackathon

<!-- widget:stepper -->

### Your rubric and tracks, locked

Criteria, weights and tracks configured per event, plus a methodology line you can publish in the rules. You get a rulebook judges and sponsors can read before the doors open.

### Submissions land on your event page

A public link or QR with a deadline and live statuses, or a manual batch you upload yourself. Completeness is checked automatically, so staff chase exceptions rather than the pile.

### The panel does the first read

Every submission scored on execution, technical depth, problem impact, innovation, UX clarity and delivery readiness — the whole field pre-read in hours.

### Every judge walks in with a briefing

Per team: scores with the evidence behind them, quotes tagged to the slide they came from, what to verify at the table, and three questions worth the four minutes. Table visits test the build instead of the pitch.

### The expo runs exactly as designed

Same tables, same judges, same closing ceremony. Judges score as usual, and where reviewers disagreed the report says so, so deliberation starts at the real argument.

### Leaderboard, then feedback for every team

The ranking is built from human Jury Scores and your criteria weights. Structured feedback is drafted from the evidence and approved by your staff before it goes out.

<!-- /widget -->

## Inputs it reads today, stated plainly

Today the panel reads what you already collect: the deck, the project description and the team's notes. Nothing changes for participants, and no judge loses a role.

<!-- widget:callout type=warning -->

**Repositories and running demos are not read today** — that is the next build on the roadmap. Anyone quoting execution scores at a closing ceremony should know what they were computed from.

<!-- /widget -->

## Monday Discord thread

A team that shipped a working build lost to a team that demoed well, and the thread is public with the sponsor cc'd. Without a record the honest answer is a shrug.

With a record, the reply is one message:

- the Execution and Demo score and its weight;
- the finding — *two of three feature claims are demonstrated; the third is described, not shown* — with its quote and slide;
- the flagged split on Technical Depth;
- the organizer's own Jury Score, logged next to the AI read.

## Disclosure kit

Hackers notice everything and post about it. The risk is defending the tool without a script.

- **Opening ceremony:** "Every submission gets a full read under identical rules, and humans decide every placement."
- **Rules page:** a methodology statement — what the panel assists with, what judges decide, how a team can ask about its own record.
- **Submission form:** plain language, so nobody discovers AI involvement after results.
- **Conflicts of interest:** your policy. The record logs who scored what, which is what makes a recusal verifiable.

## Tracks and sponsor judges

Each track scores against its own rubric, configured per event. Judge count does not go down: sponsors and alumni keep the floor and arrive briefed. Weights stay editable until the run starts, then lock so the whole field is scored on one standard.

## Data and team IP

- **Never trained on** — team submissions are processed only for your event's evaluation. Contractual.
- **Your record** — the event owns reports, scores and the decision log; retention and deletion follow your policy, and a DPA is available.
- **Institutions** — student-data handling supports an institution's obligations; PO and invoice, security questionnaires, a public sub-processor list, and an education discount for university programs.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Criteria and weights](../guides/criteria-and-weights.md) — The pitch rubric this one diverges from {sliders-horizontal}
- [Brief your jury](../guides/brief-your-jury.md) — Load arithmetic and the calibration video {users}
- [Disagreement and spread](../scoring/disagreement-and-spread.md) — What a flagged split means at the table {git-compare}

<!-- /widget -->
