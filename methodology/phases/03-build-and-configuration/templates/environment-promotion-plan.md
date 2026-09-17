# Environment Promotion Plan

## Environments

| Environment | Purpose | Data (synthetic/sampled/real) | Access Restrictions |
|---|---|---|---|
| Development | | | |
| Staging/QA | | | |
| Production | | | |

## Promotion Path

Describe the actual mechanism: config export/import, API-based promotion,
infrastructure-as-code, manual rebuild. Name the platform-specific tool (e.g.
Adobe Data Collection UI/API sandbox promotion) or note if none exists and
promotion is manual (a real and important risk to flag).

## Approval Gates

| Gate | Approver | Criteria |
|---|---|---|
| Dev → Staging | | |
| Staging → Production | | |

## Rollback Plan

- How is a bad promotion reverted? Is there a previous-version snapshot, or does
  rollback require manual reconfiguration?
- Who has authority to trigger a rollback, and how fast can it happen?

## Change Log Discipline

Every production promotion should be logged: what changed, who approved it, when,
and a link to the corresponding design doc or decision log entry. This is what
makes later "why did this change" questions answerable instead of archaeological.
