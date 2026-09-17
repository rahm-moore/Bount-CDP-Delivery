# Architecture Diagrams Guide

Diagrams are tool-agnostic in principle — reproduce these in Lucidchart, Visio,
draw.io, or Mermaid depending on the engagement's toolset. Starter Mermaid
templates are in [`templates/`](templates/) since they're plain text and easy to
version alongside the rest of this repo.

## Standard diagram types and when to produce them

| Diagram | Phase | Purpose |
|---|---|---|
| **System Context** | Discovery (draft), Design (final) | Shows every system in scope and how they relate at a high level — no internal detail. The first diagram a new stakeholder should see. |
| **Data Flow** | Design | One per major use case or data domain. Shows the actual path an event/record takes from source to destination, including transformation points. |
| **Identity Resolution Sequence** | Design | Shows, step by step, how an anonymous identity becomes a known identity and how profiles merge. |
| **Event Taxonomy Map** | Design/Build | Maps business events (e.g. "account opened") to their technical implementation (e.g. specific rule/schema field combination) across every source. |
| **Governance/RACI Org Chart** | Discovery/Handoff | Visual version of the RACI matrix — who owns what, who escalates to whom. |

## Principles

- A diagram that isn't kept current is worse than no diagram — it actively
  misleads. Update diagrams at the same time as the design docs they support, not
  as an afterthought.
- Label every box with the vendor-agnostic concept *and* the platform-specific
  name where relevant (e.g. "Collection Endpoint (Adobe: Datastream)") so the
  diagram is useful to someone unfamiliar with the specific platform.
- Keep System Context diagrams free of implementation detail — that's what Data
  Flow diagrams are for. Mixing altitude levels in one diagram makes it useless
  for both purposes.

## Starter templates

- [`templates/system-context-diagram.mmd`](templates/system-context-diagram.mmd)
- [`templates/data-flow-diagram.mmd`](templates/data-flow-diagram.mmd)
- [`templates/identity-resolution-sequence.mmd`](templates/identity-resolution-sequence.mmd)
