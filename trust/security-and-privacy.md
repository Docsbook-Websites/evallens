---
title: "EvalLens security and privacy: workspace scope and access control"
description: "Where decks live, who can read them, how access is enforced below the UI, how reports are shared, and what your IT office should ask any AI vendor that processes your submissions."
---

# Security and privacy

Pitch decks carry strategy, financials, founder details and, once a round runs, selection outcomes. This page is what happens to a deck after upload.

## Organizer-owned workspace

Evaluation runs inside a workspace owned by the organizer, with access scoped to the people and roles on that project.

- **Organizer-owned project.** In the current release each project belongs to one organizer, who owns its decks, evaluations and reports.
- **Publish gate.** Participants submit through a public page at `/e/<slug>`, and that page is public **only after the organizer publishes the project**. Before that it returns 404 — the address does not resolve to a page for anyone who guesses it.

## Access is enforced below the UI

Access is not a property of the interface. Four guardrails decide what a request can see:

| Guardrail | How it works |
|---|---|
| Session boundary | Sessions live in httpOnly cookies. Client-side scripts cannot read the token directly |
| Database rules | Postgres row-level security. An organizer can read and write only the projects tied to their account |
| Server-only keys | Service-role and AI gateway keys stay on the server. Admin operations run only after an explicit admin check |
| Public gate | The `/e/<slug>` page opens only after publication; before that, 404 |

Hiding a button is not access control, and none of the four is a UI behaviour — which answers "can a link be shared sideways?"

## Report delivery

Reports move through the organizer's workspace, never through accidental public access. A report reaches someone when the organizer shares it; participant-facing sharing is post-MVP.

## Training and ownership

- **Never trained on.** Submissions are processed only for that program's evaluation and are never used to train models. Contractual, not a setting.
- **The program owns the record.** Reports, scores and the decision log belong to the program. Retention and deletion follow your policy, and a DPA is available.
- **Education and institutional use.** Student-data handling is structured to support an institution's obligations.

## Procurement

- PO and invoice accepted.
- Vendor registration forms and security questionnaires supported.
- Public sub-processor list, published rather than supplied on request.
- Education discount for university programs.

## AI sub-processors: the question to ask every vendor

A 2026 DataGrail review found that **63.6% of vendors advertising AI never name a third-party AI sub-processor in their legal documents** (reported by VentureBeat). Your security questionnaire exists to close that gap.

EvalLens publishes its sub-processors with purpose and processing region for each, alongside the DPA and this page. Bring the questionnaire to the first conversation, not the last.

## Human decision boundary

AI prepares the analysis; the organizer reviews it, sets the final scores and decides how the report is used. That is a privacy property as well as a method: the decision affecting a team's funding, selection and reputation is made by a person who can be asked about it.

## Next steps

<!-- widget:cards plain cols=3 arrow=hover -->

- [Prompt-injection safety](./prompt-injection-safety.md) — When a deck tries to influence the evaluation {shield-check}
- [What EvalLens does not do](./boundaries.md) — The limits to state before a committee asks {shield-alert}
- [Collect submissions](../guides/collect-submissions.md) — Access settings on the submission page {inbox}

<!-- /widget -->
