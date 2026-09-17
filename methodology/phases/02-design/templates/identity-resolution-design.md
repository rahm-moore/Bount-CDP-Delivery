# Identity Resolution Design

## Identity Namespaces

| Namespace | Description | Source System(s) | Deterministic or Probabilistic | Notes |
|---|---|---|---|---|
| | | | | |

Examples: Email (hashed), Customer ID (CRM), ECID/cookie ID (Adobe) or equivalent
device ID, Login ID, Loyalty ID, Phone (hashed).

## Matching & Merge Rules

- Which namespace(s) are authoritative for merging two profiles into one?
- Deterministic matching rules (exact match on a trusted ID) vs. probabilistic
  (fuzzy match on multiple weak signals) — state which is used where, and why.
- Merge policy when two profiles with conflicting attribute values are merged
  (most-recent-wins? source-priority-wins? manual review?).
- Un-merge/split policy — what happens when a match is later proven wrong (e.g.
  shared device, family account)?

## Anonymous-to-Known Transition

- How is an anonymous (device/cookie-based) identity linked to a known (login/
  CRM-based) identity at the moment of authentication?
- Is historical anonymous activity retroactively attributed to the known profile,
  and if so, how far back?

## Privacy Boundaries

- Are there namespaces that must never be merged across (e.g. regulatory
  requirement to keep two brands' data separate)?
- Cross-border data residency constraints affecting identity resolution?
- Right-to-be-forgotten / deletion propagation — does deleting one namespace's
  data need to cascade through merged profiles?

## Platform-Specific Notes

**Adobe (RTCDP):** Identity namespaces are configured in Identity Service; merge
policies are configured per-schema in the Profile settings; use the
[glossary](../../../glossary.md) to translate this design for other platforms.

## Validation Plan

How will identity resolution accuracy be tested in Phase 04? (e.g. seed known test
identities across sources, confirm correct merge/no-merge behavior.)
