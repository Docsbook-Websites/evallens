---
title: "What EvalLens does not do"
description: "The four boundaries: it is not an external truth check, not investment advice, not automatic winner selection, and not a prediction of success. What it does instead."
---

# What EvalLens does not do

EvalLens evaluates what is present in a deck, highlights what is missing, and prepares the review. Four things it is not — worth reading before you promise anything to a committee, a sponsor or a student paper.

## It is not an external truth check

**What it does instead:** evaluates what the deck presents and flags what is missing. It does not verify claims against the outside world.

A deck that states "14 pilot customers at $190/mo" is scored on the strength and specificity of that evidence as presented. Whether those customers exist is not something a document reader can establish. False, incomplete or unsupported claims still require evidence review and, where it matters, external validation.

The same boundary applies to completeness: *missing* means the deck did not cover a section, never that a claim in it is untrue.

## It is not investment advice

**What it does instead:** gives decision support to reviewers. It is not a recommendation to fund or pass, and the output is not shaped as one.

## It is not automatic winner selection

**What it does instead:** never ranks the batch. The leaderboard is built only from submitted Jury Scores and your criterion weights; the AI Total Score sits beside them, read-only.

There is no mode in which the AI picks the winner. If a ranking changed, a person changed it.

## It is not a prediction of success

**What it does instead:** describes the pitch today. It does not forecast whether the startup will succeed, and no claim in a report should be read as one.

## The related boundary: safety is not fact-checking

Prompt-injection safety prevents instructions inside a deck from controlling the evaluation. That is a different guarantee from the deck being truthful — see [Prompt-injection safety](./prompt-injection-safety.md).

## What to say out loud

Programs that adopt an AI-assisted first read do better when they state the boundary before anyone asks, rather than defending it afterwards. Three lines that hold up:

- **On stage:** "Every entry received a full read under identical rules, and humans made every ranking decision."
- **In the rules document:** a methodology statement — what the AI panel assists with, what the judges decide, and how a team can ask about its own record.
- **On the submission form:** plain language, so nobody discovers AI involvement after the results are announced.

Judge conflict-of-interest and recusal handling stays your policy. What the record adds is that a recusal is verifiable later, because who scored what is logged.

## The honest comparison

The awkward question is not "was AI involved". It is what the alternative actually looked like: at a large competition, entry 300 drawn by a tired volunteer at 11pm; at a hackathon expo, the average judge seeing a single-digit percentage of the field in four-minute table visits. A first read under identical rules is a claim that a volunteer process cannot make — and it is compatible with humans deciding every placement.

## Next steps

- [Reproducibility](../scoring/reproducibility.md) — what has been benchmarked and what has not.
- [Security and privacy](./security-and-privacy.md) — what happens to a deck after upload.
- [Score and shortlist](../guides/score-and-shortlist.md) — where the human decision is actually made.
