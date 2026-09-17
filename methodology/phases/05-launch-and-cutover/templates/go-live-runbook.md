# Go-Live Runbook — [Engagement Name]

## Cutover Window

- Date/time (with timezone), expected duration, and why this window was chosen
  (low-traffic period, maintenance window, etc.).

## Pre-Launch Checklist

- [ ] Validation & Testing exit criteria confirmed met
- [ ] Sponsor go-live approval documented
- [ ] All stakeholders on the communications plan notified of the window
- [ ] Rollback plan reviewed by the execution team within 24 hours of cutover
- [ ] On-call/support coverage confirmed for the cutover window and monitoring period

## Cutover Steps

| Step | Action | Owner | Verification |
|---|---|---|---|
| 1 | | | |
| 2 | | | |

## Rollback Triggers

State explicit, unambiguous conditions — not "if something looks wrong."

- [ ] Example: data collection volume drops below X% of baseline within Y minutes
- [ ] Example: consent enforcement verified broken (any category)
- [ ] Example: [platform]-specific critical error rate exceeds threshold

## Rollback Procedure

Step-by-step, specific to how this engagement's promotion/config model supports
reversal (see the environment promotion plan from Phase 03).

## Communications Plan

| Audience | Message | Channel | Timing |
|---|---|---|---|
| Internal delivery team | | | Before/during/after |
| Client stakeholders | | | Before/during/after |
| Downstream teams (reporting, campaign ops) | | | Before/after |

## Post-Launch Monitoring Window

- Duration: [e.g. 48 hours active monitoring, 2 weeks passive]
- Metrics/events watched: [list specific ones derived from Phase 04 validation]
- Owner(s) and escalation path if a metric goes out of expected range.

## Sign-off

| Role | Name | Date |
|---|---|---|
| Sponsor (go-live approval) | | |
| Execution lead | | |
