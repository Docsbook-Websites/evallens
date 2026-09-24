---
title: "Score and shortlist in the Review Board"
description: "Review the batch, set human Jury Scores from 0.0 to 10.0, compare evidence, and generate a leaderboard from project weights."
status: generated
version: "0.2"
---

# Score and shortlist in the Review Board

The Review Board turns reports into a human ranking. It keeps the batch, evidence, statuses and scores in one view.

## Read the board

| Status | Meaning |
|---|---|
| `ready` | Evaluated; no Jury Score yet |
| `in review` | A reviewer is working on the entry |
| `scored` | A Jury Score has been submitted |
| `blocked` | Something prevents evaluation or scoring |

The board also shows the AI Total Score and key findings. The AI score is read-only and does not determine rank.

<!-- widget:stepper -->

### Open the report

Review the summary, evidence and findings across the criteria. Start with conflicts and weakly supported high scores.

### Ask and record

Use the criterion-linked questions in the live review. Keep notes beside the evidence they explain.

### Set Jury Scores

Score each criterion from `0.0` to `10.0`. This is separate from the AI Criterion Score.

### Generate the leaderboard

After the human scores are submitted, generate the ranking. The Final Score applies project weights to Jury Scores.

<!-- /widget -->

## Compare before deciding

Compare entries against the same criteria and inspect individual dimensions, not only the total. A lower AI score can still fit your criteria better; the human score is where that judgment belongs.

## Keep the decision trail

The round retains the AI Total Score as context, Jury Scores as the decision input, findings and slide references, and the disagreements your team discussed.

## Next steps

- [Disagreement and spread](../scoring/disagreement-and-spread.md) — Understand conflict flags.
- [Brief your jury](./brief-your-jury.md) — Prepare reviewers before scoring.
- [What EvalLens does not do](../trust/boundaries.md) — State the decision boundary.
