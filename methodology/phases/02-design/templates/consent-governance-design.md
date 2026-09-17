# Consent & Governance Design

## Consent Categories

| Category | Description | Default State (opt-in/opt-out by jurisdiction) | Enforcement Point(s) |
|---|---|---|---|
| Strictly Necessary | | Always on | |
| Functional | | | |
| Performance/Analytics | | | |
| Targeting/Advertising | | | |

## Consent Flow

- Where is consent captured (cookie banner/preference center vendor)?
- How does client-side collection read consent state before firing (e.g.
  `alloy("setConsent")` pattern, or platform equivalent)?
- How is consent state propagated server-side, if data also flows through batch/
  server-to-server paths that bypass the client-side gate?
- What happens to data collected *before* consent is granted — discarded, queued,
  or collected under a default state?

## Enforcement Verification

- How will you *prove* a given tag/collection call is actually gated by consent,
  rather than trusting the configuration? (e.g. toggle a category off in the
  preference center, confirm the corresponding call is suppressed in
  network/debug tooling.)
- Cross-reference every tag/data-collection call against its expected consent
  category — this becomes the Phase 04 validation checklist.

## Governance Labels / Data Usage Policies

- What governance labels (e.g. Adobe DULE labels, or platform equivalent) apply to
  which schema fields?
- What usage restrictions do those labels enforce (e.g. "no export to third-party
  advertising destinations")?
- Who is accountable for keeping labels correct as schemas evolve?

## Data Subject Rights

- How is a deletion/access request fulfilled across all datasets holding this
  person's data, including merged/derived profiles?
- Has this been tested end-to-end, or only designed on paper?

## Known Risk Pattern to Check For

Reversible encoding mistaken for hashing (e.g. Base64 stored under a field named
`SHA-256-HashedEmail` with no actual hash applied) is a real, previously-observed
failure mode — explicitly verify hash fields are genuinely one-way, not just
named as if they were.
