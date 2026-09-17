# Phase 00 — Discovery

## Purpose

Understand the client's current-state data landscape, stakeholders, and
constraints well enough to design a target state. This phase produces facts, not
recommendations — resist the urge to start designing here.

## Entry Criteria

- Engagement is kicked off; SOW/contract scope defines the properties/domains and
  systems in scope.
- Access requested (or granted) to: the CDP platform admin console, tag management
  system, analytics admin, and relevant source systems.

## Key Activities

- Stakeholder interviews (business, IT/data engineering, marketing/media,
  compliance/legal) — see [`templates/stakeholder-interview-guide.md`](templates/stakeholder-interview-guide.md).
- Source system inventory — every system that captures or holds customer data in
  scope — see [`templates/source-system-inventory.md`](templates/source-system-inventory.md).
- Current-state architecture mapping: what collects data, where it flows, what
  transforms it, where it lands, what consumes it.
- Consent/privacy posture review: what consent management platform is in use, what
  categories exist, how (or whether) enforcement is verified today.
- RACI baseline for the engagement — see [`templates/raci-matrix-template.md`](templates/raci-matrix-template.md).
- Identify known pain points, technical debt, and "tribal knowledge" gaps (systems
  nobody currently understands fully).

## Deliverables Checklist

- [ ] Stakeholder map with roles and interview notes
- [ ] Source system inventory (complete, validated with the client)
- [ ] Current-state architecture diagram (see [`../../diagrams/README.md`](../../diagrams/README.md) — System Context diagram)
- [ ] Consent/privacy posture summary
- [ ] RACI matrix (draft, to be refined through later phases)
- [ ] Known-gaps/technical-debt log
- [ ] Discovery findings summary presented back to the client for validation

## Exit Criteria

- The client has confirmed the current-state architecture diagram and source
  inventory are accurate — not just delivered, *confirmed*.
- No major "unknown unknowns" remain about what systems exist in scope (unknowns
  about *how* something works are fine — those get resolved in Design).

## Common Pitfalls

- Treating a vendor's own documentation as ground truth without validating against
  what's actually configured live (admin consoles lie less than wikis).
- Skipping compliance/legal stakeholders because "this is a technical project" —
  consent and governance requirements discovered late are expensive to retrofit.
- Under-scoping the source inventory to only digital/web sources when CRM, batch/
  offline, and call-center systems are just as often in scope for identity
  resolution and profile unification.

## Look Ahead (what Strategy & Use Cases will need from you)

- The source inventory becomes the input to feasibility scoring for use cases —
  make sure it notes *data quality* and *access constraints* per source, not just
  existence.
- Stakeholder interviews should surface candidate use cases even though
  prioritizing them isn't this phase's job — capture them, don't lose them.
