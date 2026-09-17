# Integration Architecture

## Sources

| Source System | Collection Method | Auth Model | Frequency (real-time/batch/interval) | Target Schema/Dataset | Notes |
|---|---|---|---|---|---|

## Destinations

| Destination | Activation Method | Data Sent (which segments/attributes) | Frequency | Owner | Notes |
|---|---|---|---|---|---|

## Data Flow Summary

Reference the Data Flow diagram(s) in [`../../diagrams/`](../../diagrams/) — this
section is the narrative walkthrough, the diagram is the visual.

## Latency & SLA Requirements

| Use Case | Required Latency | Actual Platform Capability | Gap? |
|---|---|---|---|

## Environment Topology

- List environments (dev/staging/prod, or platform-specific equivalents —
  sandboxes, workspaces).
- State whether each source/destination integration exists per-environment or is
  shared (e.g. a single production-only destination with no non-prod equivalent —
  a common and important gap to surface early).

## Dependency Risks

- Third-party API rate limits, auth token expiry/rotation requirements, vendor
  contract constraints on data usage — log material ones in the
  [risk register](../../../risk-register/risk-register-template.md).
