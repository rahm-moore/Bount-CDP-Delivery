# QA Test Plan

## Test Categories

| Category | Description | In Scope? |
|---|---|---|
| Event/data collection accuracy | Events fire correctly, with correct field values, on the correct triggers | |
| Identity resolution | Known test identities merge/don't merge as designed | |
| Consent enforcement | Data collection correctly gated by consent state, per category | |
| Schema conformance | Payloads validate against schema; no unexpected nulls/types | |
| Destination/activation | Segments/audiences activate correctly to each destination | |
| Cross-environment consistency | Dev/staging/prod configs match except for intentional environment-specific differences | |
| Load/volume | Platform handles expected production volume without data loss or excessive latency | |

## Test Case Template

| ID | Category | Precondition | Steps | Expected Result | Actual Result | Pass/Fail | Notes |
|---|---|---|---|---|---|---|---|

## Severity Definitions

- **Critical** — blocks go-live; data loss, PII exposure, or consent enforcement
  failure.
- **High** — significant functional gap in an in-scope use case; workaround may
  exist but is not acceptable long-term.
- **Medium** — noticeable but non-blocking; scheduled for near-term post-launch fix.
- **Low** — cosmetic or edge-case; backlog item.

## Sign-off

| Role | Name | Date | Recommendation (Go / No-Go / Go with exceptions) |
|---|---|---|---|
