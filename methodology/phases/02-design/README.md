# Phase 02 — Design

## Purpose

Architect the target state: identity resolution, canonical schema, consent
enforcement, and system integrations. This is the phase where "we should build a
CDP" becomes a specific, reviewable, buildable architecture.

## Entry Criteria

- Prioritized use case list with sponsor sign-off (Phase 01).
- Cross-cutting technical requirements list from Phase 01.

## Key Activities

- Identity resolution design — namespaces, matching/merge rules, privacy
  boundaries — see [`templates/identity-resolution-design.md`](templates/identity-resolution-design.md).
- Canonical schema / data model design — see
  [`templates/schema-data-model-design.md`](templates/schema-data-model-design.md)
  (Adobe XDM variant included).
- Consent & governance design — how consent is captured, enforced, and audited —
  see [`templates/consent-governance-design.md`](templates/consent-governance-design.md).
- Integration architecture — sources, destinations, data flow, latency/SLAs — see
  [`templates/integration-architecture.md`](templates/integration-architecture.md).
- Architecture diagrams: System Context, Data Flow, Identity Resolution Sequence —
  see [`../../diagrams/README.md`](../../diagrams/README.md).
- Environment strategy (dev/stage/prod topology, promotion model) — drafted here,
  finalized in Build.
- Design review with client architecture/IT stakeholders; capture decisions in the
  [decision log](../../decision-log/decision-log-template.md).

## Deliverables Checklist

- [ ] Identity resolution design, reviewed and approved
- [ ] Canonical schema / data model design, reviewed and approved
- [ ] Consent & governance design, reviewed and approved
- [ ] Integration architecture doc, reviewed and approved
- [ ] System Context diagram
- [ ] Data Flow diagram(s), one per major use case or data domain
- [ ] Identity Resolution sequence diagram
- [ ] Environment strategy draft
- [ ] Decision log entries for every non-obvious design choice
- [ ] Design walkthrough delivered to and approved by the client

## Exit Criteria

- All four design documents (identity, schema, consent, integration) are approved
  by the client's technical stakeholder(s).
- No open design questions block starting Build — anything unresolved is logged
  as a risk with an owner and target resolution date, not silently deferred.

## Common Pitfalls

- Designing the schema before the identity resolution strategy is settled — identity
  namespaces are inputs to schema design (e.g. which fields carry which ID types),
  not an afterthought.
- Treating consent design as a compliance checkbox instead of an architecture
  concern — consent state needs to flow through the same pipees as the data it
  gates, or enforcement can't be verified.
- Designing for the platform's default/demo configuration instead of the client's
  actual scale, latency, and governance requirements.
- Skipping the "why" in the decision log — a schema or identity choice that looks
  wrong in six months, with no recorded rationale, gets re-litigated or reverted
  incorrectly.

## Look Ahead (what Build will need from you)

- Design docs need to be specific enough to configure directly from: exact schema
  fields and types, exact identity namespace names, exact consent category
  mappings, exact source/destination list with auth requirements.
- Flag anything that needs a platform capability not yet confirmed available (e.g.
  a specific identity stitching rule the platform may not support out of the box)
  — Build needs to know this before, not during, configuration.
