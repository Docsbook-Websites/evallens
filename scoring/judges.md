---
title: "EvalLens AI judges: six lenses and the routing matrix"
description: "What each of the six AI judge lenses reads, why they never see one another's scores, and how much each one influences each dimension — primary, secondary, advisory or not scored."
status: generated
version: "0.1"
---

# AI judges and the routing matrix

Six independent AI judges read every pitch deck, each through its own lens. They work in isolated contexts and never see one another's scores; where they disagree, the report says so instead of averaging it away.

## Six judge lenses

| Judge | Reads |
|---|---|
| **J-P1 Problem** | The pain, the user, the urgency, and the alternatives a deck claims to beat |
| **J-P2 Solution Logic** | Product logic, differentiation, and how coherently the solution holds together |
| **J-P3 Business Value / Market** | The market, the value, and how the business intends to make money |
| **J-P4 Pitch Quality** | Clarity, narrative, structure and delivery |
| **J-P5 Team Readiness** | Founder-market fit, skills, and the ability to execute |
| **J-P6 Feasibility** | Roadmap, resources, and operational realism |

## Not every judge influences every score

A lens contributes to a dimension at one of four levels: **primary** (1.00) drives the score, **secondary** (0.50) adds important support, **advisory** (0.25) provides context, and **not scored** means no influence at all.

| Judge | P1 Problem | P2 Solution | P3 Market | P4 GTM | P5 Team | P6 Feasibility |
|---|---|---|---|---|---|---|
| J-P1 Problem | primary | advisory | advisory | — | — | advisory |
| J-P2 Solution Logic | secondary | primary | advisory | advisory | — | secondary |
| J-P3 Business Value / Market | advisory | advisory | primary | primary | — | advisory |
| J-P4 Pitch Quality | advisory | advisory | advisory | advisory | advisory | advisory |
| J-P5 Team Readiness | — | — | advisory | advisory | primary | secondary |
| J-P6 Feasibility | advisory | secondary | secondary | secondary | secondary | primary |

Two things to read off this table:

**Pitch Quality is advisory everywhere.** It is visible in the report and it never drives a dimension. This is the structural answer to "does a polished deck win here?" — presentation quality matters, but it cannot outrank weak evidence on problem, market, team or feasibility.

**Team Readiness does not score Problem or Solution.** A lens only scores where it has a legitimate read. That is what keeps a strong impression of the founders from bleeding into every dimension.

## Independence by structure: isolated contexts

Each judge evaluates in an isolated context. Three consequences:

- **No anchoring.** A lens cannot converge on another's number, so agreement between them is evidence rather than an artifact.
- **Halo effect is split.** Dimensions are read by separate judges, so one strong impression cannot carry the whole scorecard.
- **Containment.** An instruction hidden in a deck that reaches one context cannot reach another. See [Prompt-injection safety](../trust/prompt-injection-safety.md).

## Other bias controls

| Risk | Control |
|---|---|
| Halo effect | Dimensions split across separate judges |
| Generic scoring | Dimension-specific prompts and criteria per judge |
| Overweighting presentation | Pitch Quality visible, never dominant |
| Hidden disagreement | Spread plus the judge contribution matrix |
| AI overreach | The AI Total Score is advisory; the human decides |
| Assumption-filling | Missing evidence becomes a gap or a question, never a guess |

## Method origin: three startup-evaluation lenses

The Pitch Competition dimension matrix combines three established startup-evaluation lenses rather than being assembled from prompt tricks:

- **Lean Startup** — hypothesis and problem-solution logic, feeding P1 and P2.
- **Customer Development** — customer, pain and validation evidence, feeding P1 and P2.
- **VC Due Diligence** — market, business model, team and feasibility, feeding P3, P5 and P6.

It is thesis-first by design: a polished deck should not score high if the problem is vague, the customer unclear and the business logic thin.

## Hackathon panel: five reviewer roles

<!-- widget:callout type=note -->

**Running a hackathon?** Hackathon mode uses five reviewer roles — Innovation, Technical Execution, Business Value, Pitch Quality and Feasibility — on an execution-weighted rubric. See [Hackathons](../use-cases/hackathons.md).

<!-- /widget -->

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Dimensions P1–P6](./dimensions.md) — The six questions and their anchors {list-checks}
- [Score calculation](./how-the-score-is-built.md) — How routing weights make one number {sigma}
- [Disagreement and spread](./disagreement-and-spread.md) — When the lenses do not agree {git-compare}

<!-- /widget -->
