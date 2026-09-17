# Phase 05 — Launch & Cutover

## Purpose

Go live, safely, with a clear rollback path and a defined monitoring window. This
phase is short in duration but highest in blast radius — the runbook exists so
nothing critical depends on memory under pressure.

## Entry Criteria

- Validation & Testing exit criteria met; go/no-go recommendation reviewed.
- Sponsor has given explicit go-live approval.

## Key Activities

- Build the go-live runbook — see
  [`templates/go-live-runbook.md`](templates/go-live-runbook.md).
- Define and rehearse the rollback plan — what triggers a rollback, who decides,
  how fast can it execute.
- Define the post-launch monitoring window: what metrics/events are watched, at
  what frequency, by whom, for how long.
- Communications plan: who needs to know before, during, and after cutover
  (internal team, client stakeholders, downstream teams affected by the change).
- Execute cutover during the agreed window.
- Monitor actively through the defined window; do not consider launch "done" the
  moment configuration is live.

## Deliverables Checklist

- [ ] Go-live runbook, reviewed and rehearsed
- [ ] Rollback plan with clear trigger conditions and owner
- [ ] Communications plan executed
- [ ] Cutover executed
- [ ] Post-launch monitoring window completed with no unresolved Critical issues

## Exit Criteria

- Production is live, stable, and has passed through the defined monitoring
  window without triggering rollback.
- Any issues found during the monitoring window are logged and triaged (fixed,
  scheduled, or accepted).

## Common Pitfalls

- No rollback plan because "we tested thoroughly" — validation reduces risk, it
  doesn't eliminate the need for a way back.
- Treating go-live as the finish line and disbanding the team's attention before
  the monitoring window closes — many real issues surface at production volume/
  timing patterns that non-prod testing can't fully replicate.
- Cutting over without informing downstream teams who consume the data (reporting,
  campaign ops) — they discover the change by their own reports breaking.

## Look Ahead (what Handoff & Optimization will need from you)

- A record of what actually happened during cutover (any deviations from the
  runbook, any issues hit and how resolved) — this becomes part of the handoff
  package and prevents relitigating "why is it configured this way" later.
- Monitoring window findings that are deferred (not fixed pre-launch) need to
  carry forward explicitly into the post-launch optimization roadmap.
