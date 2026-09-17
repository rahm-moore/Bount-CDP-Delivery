# Phase 04 — Validation & Testing

## Purpose

Prove the build matches the design and the data flowing through it is trustworthy
— before, not after, go-live. This is the phase where "it looks like it's working"
gets replaced with "here's the evidence it's working."

## Entry Criteria

- Build exists in at least one testable non-prod environment (ideally
  production-like).

## Key Activities

- Execute the QA test plan — see [`templates/qa-test-plan.md`](templates/qa-test-plan.md).
- Run data quality validation — see
  [`templates/data-quality-validation-checklist.md`](templates/data-quality-validation-checklist.md).
- Validate identity resolution against the test plan defined in the identity
  design doc (seed known test identities, confirm correct merge/no-merge).
- Validate consent enforcement per-tag/per-call against the consent design doc
  (toggle categories, confirm suppression).
- Validate schema conformance (sampled payloads match schema, required fields
  populated, no unexpected nulls at volume).
- Load/volume testing if the use cases have meaningful scale or latency
  requirements.
- Document every finding as a gap with severity — feed confirmed gaps into the
  engagement's gap/risk tracking (see
  [risk register](../../risk-register/risk-register-template.md)).

## Deliverables Checklist

- [ ] QA test plan executed with results recorded
- [ ] Data quality validation complete
- [ ] Identity resolution validated against defined test cases
- [ ] Consent enforcement validated tag-by-tag/call-by-call
- [ ] Schema conformance validated
- [ ] Gap list compiled with severity and owner
- [ ] Go/no-go recommendation prepared for the sponsor

## Exit Criteria

- All Critical and High severity gaps are resolved or have an explicit,
  sponsor-accepted deferral with a documented reason.
- The go/no-go recommendation has been reviewed by the client's technical and
  business stakeholders.

## Common Pitfalls

- Testing only the happy path (a single test user, one browser, ideal network
  conditions) and missing edge cases that show up immediately in production scale.
- Treating "the dashboard shows data" as validation, without confirming the data
  is *correct*, not just *present*.
- Skipping consent enforcement re-validation after any build change, even a small
  one — consent gating is easy to accidentally break during unrelated fixes.
- Declaring "done" on a gap list that still has open Critical items, under
  schedule pressure, without an explicit sponsor decision to accept that risk.

## Look Ahead (what Launch & Cutover will need from you)

- A clean (or explicitly risk-accepted) validation record to justify the go/no-go
  decision.
- Specific monitoring checks derived from validation (e.g. "watch this specific
  event volume for the first 48 hours") feed directly into the go-live runbook's
  post-launch monitoring section.
