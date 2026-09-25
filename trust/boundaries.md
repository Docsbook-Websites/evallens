---
title: "What EvalLens does not do"
description: "The four boundaries: it is not an external truth check, not investment advice, not automatic winner selection, and not a prediction of success. What it does instead."
---

# What EvalLens does not do

EvalLens evaluates what is in a deck, flags what is missing, and prepares the review. Here are the four things it is not; read them before you promise a committee, a sponsor or a student paper anything.

## Not an external truth check

**What it does instead:** evaluates what the deck presents and flags what is missing. It does not verify claims against the outside world.

A deck stating "14 pilot customers at $190/mo" is scored on how strong and specific that evidence is as presented. Whether the customers exist is not something a document reader can establish; where it matters, validate externally.

The same boundary applies to completeness: *missing* means the deck did not cover a section, never that a claim in it is untrue.

## Not investment advice

**What it does instead:** gives decision support to reviewers. It is not a recommendation to fund or pass, and the output is not shaped as one.

## Not automatic winner selection

**What it does instead:** never ranks the batch. The leaderboard is built only from submitted Jury Scores and your criterion weights; the AI Total Score sits beside them, read-only.

There is no mode in which the AI picks the winner. If a ranking changed, a person changed it.

## Not a prediction of success

**What it does instead:** describes the pitch today. It does not forecast whether the startup will succeed, and no claim in a report should be read as one.

## Safety is not fact-checking

Prompt-injection safety prevents instructions inside a deck from controlling the evaluation. That is a different guarantee from the deck being truthful — see [Prompt-injection safety](./prompt-injection-safety.md).

## Boundary wording to say out loud

State the boundary before anyone asks rather than defending it afterwards. Three lines that hold up:

- **On stage:** "Every entry received a full read under identical rules, and humans made every ranking decision."
- **In the rules document:** a methodology statement — what the AI panel assists with, what the judges decide, and how a team can ask about its own record.
- **On the submission form:** plain language, so nobody discovers AI involvement after the results are announced.

Judge conflict-of-interest and recusal handling stays your policy. What the record adds is that a recusal is verifiable later, because who scored what is logged.

## Comparison with the unassisted first read

The real question is not "was AI involved" but what the alternative looked like: entry 300 drawn by a tired volunteer at 11pm, or a hackathon judge seeing a single-digit share of the field in four-minute table visits. A first read under identical rules is a claim a volunteer process cannot make, and humans still decide every placement.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Reproducibility](../scoring/reproducibility.md) — What has been benchmarked, and what has not {repeat}
- [Security and privacy](./security-and-privacy.md) — What happens to a deck after upload {lock}
- [Score and shortlist](../guides/score-and-shortlist.md) — Where the human decision is made {gavel}

<!-- /widget -->
