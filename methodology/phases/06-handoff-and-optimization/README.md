# Phase 06 — Handoff & Optimization

## Purpose

Transfer real ownership to the client and establish the operating model that
keeps the implementation healthy after the delivery team leaves. A CDP that only
the delivery team understands is not actually delivered.

## Entry Criteria

- Production is live and has passed the post-launch monitoring window (Phase 05).

## Key Activities

- Assemble and deliver the handoff package — see
  [`templates/handoff-package-checklist.md`](templates/handoff-package-checklist.md).
- Define the post-launch governance/operating model — see
  [`templates/governance-operating-model.md`](templates/governance-operating-model.md).
- Knowledge transfer sessions with the client team who will own day-to-day
  operations.
- Establish a post-launch optimization roadmap — deferred gaps from Phase 04,
  known technical debt, and next-phase use cases from Phase 01's sequencing.
- Formal handoff acceptance from the client.

## Deliverables Checklist

- [ ] Handoff package delivered (architecture diagrams, schema docs, runbooks,
      decision log, risk register — all current, not stale)
- [ ] Governance/operating model documented and agreed
- [ ] Knowledge transfer sessions completed
- [ ] Post-launch optimization roadmap documented
- [ ] Formal handoff acceptance signed by the client

## Exit Criteria

- The client has formally accepted handoff.
- The client's own team can answer "who owns this, and what's the process to
  change it" without needing the delivery team.

## Common Pitfalls

- Handing off documentation that describes the *design* intent rather than the
  *as-built* state — reconcile these before handoff, don't leave it as a discovery
  exercise for the client.
- No named owner for ongoing governance (schema changes, new destination
  approvals, consent category changes) — decisions default to whoever touches it
  next, with no consistency.
- Treating handoff as a document drop instead of a conversation — knowledge
  transfer needs live sessions, not just links to files.

## Look Ahead

This is the last phase in this delivery cycle, but rarely the last phase of the
relationship. The optimization roadmap often seeds the next engagement's Phase 01
(Strategy & Use Cases) — keep it concrete and prioritized, not a vague wishlist.
