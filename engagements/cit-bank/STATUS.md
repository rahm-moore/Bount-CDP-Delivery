# Engagement Status — CIT Bank

**Platform:** Adobe AEP / RTCDP / WebSDK (Alloy.js), Adobe Analytics, Adobe Launch/Tags, GTM
**Engagement start:** see `cit-bank-websdk` repo history (pre-2026 Phase 1 kickoff)
**Last updated:** 2026-09-16

## Current Phase

**Phase 02 — Design** — see
[`../../methodology/phases/02-design/README.md`](../../methodology/phases/02-design/README.md)

Phase 1 (Discovery and Assessment) is complete. Full scope/property definitions:
[`PROJECT_SCOPE.md`](PROJECT_SCOPE.md).

## Phase Progress

| Phase | Status | Notes |
|---|---|---|
| 00 — Discovery | Complete | Current-state architecture, source inventory, and property scope documented across CAS-894/CAS-933/CAS-936 audits. Full detail lives in the `cit-bank-websdk` repo (this engagement's detailed working archive — not duplicated here). |
| 01 — Strategy & Use Cases | Complete | OAO ("Open Account Online") confirmed as the Phase 2 pilot, including all Wealth sub-flows (SD/Advised/Guided Investing). |
| 02 — Design | In Progress | Pilot scope: OAO only. D1 (authenticated post-login UX) explicitly deferred; cit.com deferred, planned concurrent with D1 post-OAO. |
| 03 — Build & Configuration | Not Started | |
| 04 — Validation & Testing | Not Started | |
| 05 — Launch & Cutover | Not Started | |
| 06 — Handoff & Optimization | Not Started | |

## Current Phase — Deliverables Checklist (Design, OAO scope)

- [ ] Identity resolution design for OAO (incl. Wealth SD/Advised/Guided Investing)
- [ ] Canonical schema / XDM design for OAO flows
- [ ] Consent & governance design for OAO (OneTrust × GTM × Adobe alignment —
      see CAS-1007 in `cit-bank-websdk`)
- [ ] Integration architecture for OAO
- [ ] Design walkthrough approved by client

## Open Risks / Blockers

- Cookie consent page-by-page validation (CAS-1007) still open for OAO routes —
  31 application routes flagged "Review," not yet confirmed pass/fail.
- PII exposure finding (reversible Base64 mistaken for a hash under
  `SHA-256-HashedEmail`) — not yet ticketed as of last sync; needs a Risk Register
  entry. See the "Known Risk Pattern" note in
  [`../../methodology/phases/02-design/templates/consent-governance-design.md`](../../methodology/phases/02-design/templates/consent-governance-design.md).
- Full risk/decision history lives in the `cit-bank-websdk` repo
  (`docs/decisions/`, `docs/investigations/`) — this file is a status summary, not
  a duplicate of that record.

## Next Steps

1. Complete OAO-scope Design deliverables above before moving to Build.
2. Resolve CAS-1007's remaining OAO acceptance criteria (per-route confirmation,
   CAS-929 gap sync) — these are Phase 02 exit-criteria-adjacent even though the
   ticket itself is framed as a validation task.
3. Once OAO Design is approved, do **not** pull in D1/cit.com Design work — they
   are explicitly sequenced after OAO per client direction (2026-09-16); revisit
   this file's Phase Progress table when that sequencing changes.

## Cross-reference

The full detailed working record for this engagement (investigations, decisions,
meeting notes, ticket-by-ticket history) lives in the separate `cit-bank-websdk`
repo — that repo is the durable archive; this file is a status summary aligned to
the methodology's phase model.
