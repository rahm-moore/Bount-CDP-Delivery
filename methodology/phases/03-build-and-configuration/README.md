# Phase 03 — Build & Configuration

## Purpose

Implement the approved design across environments: configure schemas, identity
resolution, consent enforcement, and integrations so a non-prod environment
matches the design doc exactly.

## Entry Criteria

- Design docs (identity, schema, consent, integration) approved by the client.
- Environment access provisioned (dev/staging at minimum).

## Key Activities

- Configure schemas/datasets per the schema design doc.
- Configure identity namespaces and merge policies per the identity design doc.
- Configure collection (client-side data layer, tag management rules, server-side
  connectors) per the integration architecture doc.
- Configure consent enforcement per the consent design doc.
- Configure destinations/activation per the integration architecture doc.
- Build out environment promotion process — see
  [`templates/environment-promotion-plan.md`](templates/environment-promotion-plan.md).
- Track every build decision that deviates from the design doc — update the design
  doc and the [decision log](../../decision-log/decision-log-template.md); don't let
  build-time reality silently diverge from documentation.

## Deliverables Checklist

- [ ] Schemas/datasets configured in at least one non-prod environment
- [ ] Identity namespaces and merge rules configured
- [ ] Collection (client-side + server-side as applicable) implemented
- [ ] Consent enforcement implemented and wired to the data layer
- [ ] Destinations/activation configured
- [ ] Environment promotion plan documented and, ideally, exercised at least once
- [ ] Design docs updated to reflect any build-time deviations

## Exit Criteria

- Non-prod build matches the design doc (or the design doc has been updated to
  match a justified, logged deviation).
- Build is ready for systematic validation — not just "looks right when I click
  around."

## Common Pitfalls

- Configuring against the platform's easiest default instead of the design doc's
  actual specification, then forgetting to reconcile.
- No environment promotion discipline — configuring directly in production because
  "it's faster," creating an unrepeatable, undocumented production state.
- Losing track of *why* a build-time choice deviated from design — six months
  later this reads as a bug, not a decision.

## Look Ahead (what Validation & Testing will need from you)

- A specific, versioned build state (environment name, config version/timestamp)
  to test against.
- The consent design's enforcement points, so Validation knows exactly which tags/
  calls to test toggling categories against.
