# Project Scope — CIT Bank WebSDK/CDP Delivery (Phase 2 — Design)

_Canonical scope reference, client-confirmed 2026-09-16. Read this before assuming
which property (OAO / D1 / cit.com) is in scope for current work._

This repo hosts delivery tooling (e.g. `aep-promotion-form.html`) supporting the CIT
Bank AEP/RTCDP WebSDK engagement. The fuller working archive — investigations,
decisions, ticket index — lives in the `cit-bank-websdk` repo; this file exists so
this repo doesn't drift out of sync on scope basics.

## Property / flow definitions

- **OAO = "Open Account Online."** The bank's open-account onboarding flow on the
  public website. **This is the current WebSDK migration pilot (Phase 2).**
- **OAO includes all Wealth management sub-flows** — Wealth is a product option
  presented during account opening, not a separate property. Three variations, all
  in scope as part of the OAO pilot:
  - Wealth **SD** (Standard)
  - Wealth **Advised**
  - Wealth **Guided Investing**
- **D1** = the site's *authenticated* experience — pages/features shown to a visitor
  after logging in. D1 is for **current customers'** post-authentication UX, not
  onboarding.
- **cit.com** = the bank's regular/marketing site pages — non-authenticated,
  non-onboarding.

## Phase scope

- **Phase 1 (Discovery and Assessment):** complete.
- **Phase 2 (Design) — current phase, as of 2026-09-16.**
- **OAO is the sole pilot for Phase 2**, including all Wealth sub-flows.
- **D1 is explicitly out of scope**, deferred until the OAO WebSDK build is
  complete.
- **cit.com** is the remaining property; planned to be worked **concurrently with
  D1** once the OAO WebSDK build finishes (stated planning intent, not yet
  scheduled/committed work).

## Why this matters

Phase 2's purpose is not an exhaustive audit or build-out of every property — it's
narrower: validate/design OAO (including Wealth) enough to stand up CJA reporting
and compare it against legacy AA, to support a decision on sunsetting legacy AA.
Any tooling or delivery work in this repo should default to OAO scope unless a
task explicitly says otherwise.

## Full reference

Full rationale and cross-references: `cit-bank-websdk` repo,
`docs/decisions/2026-09-16-oao-pilot-scope-and-property-definitions.md`.
