# Phase 01 — Strategy & Use Cases

## Purpose

Turn Discovery's raw findings into a prioritized, funded list of use cases the CDP
implementation will actually be designed to serve. A CDP with no prioritized use
case is a very expensive database.

## Entry Criteria

- Discovery is complete and validated with the client (current-state architecture,
  source inventory, stakeholder map).
- Candidate use cases captured during Discovery interviews are compiled into a
  single list.

## Key Activities

- Score and prioritize candidate use cases — see
  [`templates/use-case-prioritization-matrix.md`](templates/use-case-prioritization-matrix.md).
- For each prioritized use case, build a lightweight business case (expected value,
  cost/effort, dependencies) — see
  [`templates/business-case-template.md`](templates/business-case-template.md).
- Identify cross-cutting requirements implied by the use case list (e.g. "real-time
  personalization" implies streaming ingestion; "cross-device identity" implies a
  specific identity resolution strategy) — these become Design-phase constraints.
- Validate use cases against the Discovery-phase data quality/access findings —
  a use case that needs data you can't reliably get isn't ready yet.
- Get executive sponsor sign-off on the prioritized list and its sequencing.

## Deliverables Checklist

- [ ] Use case prioritization matrix, scored and ranked
- [ ] Business case per top-tier use case
- [ ] Cross-cutting technical requirements list (feeds Design phase constraints)
- [ ] Use case sequencing/roadmap (what ships in which release)
- [ ] Executive sign-off on prioritized list

## Exit Criteria

- A ranked, scoped, sponsor-approved use case list exists.
- Each in-scope use case has a named business owner.
- Known data gaps blocking a use case are either resolved or explicitly deferred
  (with the use case moved to a later release).

## Common Pitfalls

- Prioritizing by "loudest stakeholder" instead of a consistent scoring method —
  breeds later disputes about why X shipped before Y.
- Approving a use case that depends on data flagged "unclear" or "poor quality" in
  Discovery without a plan to close that gap first.
- Under-specifying use cases to a one-line wish ("personalization") instead of a
  concrete, testable outcome ("show a different homepage hero based on account
  status within 200ms of page load").

## Look Ahead (what Design will need from you)

- Each use case should be specific enough that a Designer can derive: what events/
  attributes it needs, what identity resolution it requires (single-device? cross-
  device? authenticated-only?), what activation destinations it needs, and what
  latency it requires (real-time vs. batch).
