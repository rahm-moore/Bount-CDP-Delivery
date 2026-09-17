# Canonical Schema / Data Model Design

## Schema Inventory

| Schema Name | Class (Event/Profile/Lookup) | Purpose | Datasets Using It | Status |
|---|---|---|---|---|
| | | | | |

## Field Design (per schema)

| Field Path | Data Type | Identity Namespace? | PII? | Source | Notes |
|---|---|---|---|---|---|
| | | | | | |

## Design Principles

- Prefer extending an existing standard schema/mixin over inventing new field
  structures from scratch, unless the standard genuinely doesn't fit.
- Every PII field must map to a governance label and a consent category (see
  [`consent-governance-design.md`](consent-governance-design.md)).
- Version schemas explicitly — a breaking field change needs a new schema version
  and a migration plan for existing datasets, not a silent overwrite.
- Design for the union of near-term use cases, not just the first release — but
  don't add speculative fields with no use case behind them.

## Platform-Specific Notes

**Adobe (AEP XDM):** Use XDM Individual Profile / ExperienceEvent base classes;
prefer standard mixins (e.g. `_experience`, commerce mixins) before custom field
groups; document the schema's field group composition and any custom field group
namespace (`_<tenantId>`).

**Vendor-agnostic equivalent:** "canonical schema" as used elsewhere in this
methodology — see [glossary](../../../glossary.md) for the term mapping across
Segment (Tracking Plan), Tealium (Data Source Schema), mParticle (Data Plan), and
Salesforce Data Cloud (Data Model Object).

## Validation Plan

How will schema correctness be tested in Phase 04? (e.g. sample payload validation
against schema, field-level data quality checks post-ingestion.)
