# Source System Inventory

One row per system that captures, holds, or transforms customer data in scope.

| System | Type (web/mobile/CRM/POS/call-center/batch/other) | Owner (team/vendor) | Data Captured | Integration Method (SDK/API/batch file/webhook) | Contains PII? | Data Quality Notes | Access Status |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

## Field guidance

- **Data Captured** — be specific: "email, name, transaction amount" not "customer data."
- **Integration Method** — this drives Design-phase integration architecture; note
  auth model (OAuth, API key, SFTP credentials) if known.
- **Contains PII?** — flag Yes/No/Unclear. "Unclear" is a valid, important answer —
  it becomes a Discovery follow-up, not a guess.
- **Data Quality Notes** — known issues: duplicate records, missing fields, stale
  data, inconsistent formats across environments.
- **Access Status** — Requested / Granted / Denied / Not yet requested. Track this
  actively; it's often the actual critical path in Discovery.

## Roll-up questions to answer once the table is complete

- Which systems are authoritative for identity (source of truth for a given ID type)?
- Which systems have no owner who can speak to them confidently?
- Which systems are candidates for retirement/consolidation post-migration?
