# Cross-Platform Glossary

The same architectural concept has a different name on every CDP platform. Use this
to translate a template written with one vendor's vocabulary into another's, and to
recognize when two platforms are describing the same thing.

| Concept | Adobe (AEP / RTCDP / WebSDK) | Segment | Tealium (AudienceStream/EventStream) | mParticle | Salesforce Data Cloud | Generic term to use in vendor-agnostic docs |
|---|---|---|---|---|---|---|
| Client-side collection endpoint/config | Datastream | Source (device-mode/cloud-mode) | Data Source / Collector | Input | Data Stream | **Collection endpoint** |
| Canonical event/record schema | XDM Schema | Protocols Tracking Plan | Data Source Schema | Data Plan | Data Model Object (DMO) | **Canonical schema** |
| Raw event storage | Dataset | Warehouse table / raw event stream | Data Store | Data Warehouse export | Data Lake Object (DLO) | **Event/record dataset** |
| Person-level identifier type | Identity Namespace | External ID type | Visitor ID type | Identity Type | Identity Resolution Ruleset field | **Identity namespace** |
| Unified person record | Unified Profile / Real-Time Customer Profile | Unify (Personas) profile | AudienceStream visitor profile | User profile | Unified Individual | **Unified profile** |
| Grouped audience for activation | Segment / Audience | Audience (Engage) | Audience | Audience | Segment | **Segment/audience** |
| Where activated data is sent | Destination | Destination | Connector | Output / Audience connection | Data Action / Activation Target | **Destination** |
| Consent state tracking | Consent object in XDM + Web SDK `setConsent` | Consent Manager | Consent Manager (OneTrust integration pattern) | Consent state via SDK | Consent API | **Consent record** |
| Client-side data collection layer | `alloy.js` (Web SDK) / `_satellite` (Launch/Tags legacy) | Analytics.js | `utag.js` | Web SDK / native SDKs | Web/Mobile SDK | **Client-side data layer** |
| Tag management system | Adobe Experience Platform Tags (formerly Launch) | (not applicable — Segment is itself the layer) | Tealium iQ Tag Management | (typically paired with GTM or similar) | (typically paired with GTM or similar) | **Tag management system (TMS)** |
| Reporting/analysis layer built on the CDP | Customer Journey Analytics (CJA) | (Segment + a BI tool) | Tealium + a BI tool | mParticle + a BI tool | Tableau / CRM Analytics | **Analytics/reporting layer** |
| Config promotion between environments | Sandbox promotion (Data Collection UI / API) | Workspace environments | Tealium environments (dev/qa/prod) | Environments (dev/prod) | Org-based sandbox/promotion | **Environment promotion** |
| Data governance labels | DULE labels (Data Usage Labeling & Enforcement) | Protocols governance / PII flags | Consent/PII tagging | Data Subject Request tooling | Data governance policies | **Governance label** |

## Using this table

- When writing a **vendor-agnostic** template (used across all engagements), use the
  Generic term column and note the platform-specific term as a parenthetical example.
- When writing an **Adobe-specific** template variant, use Adobe's actual terms —
  don't force generic language where it reduces precision for that platform.
- Add a row whenever you onboard a new platform and hit a term that isn't mapped yet.
