# The Data Systems Architect Bible

A vendor-agnostic methodology for delivering a Customer Data Platform (CDP)
implementation from **Discovery to Handoff**. Built from real engagement experience
(originally Adobe AEP/RTCDP/WebSDK), generalized so it works for any platform where
the same underlying architecture problems show up: data collection, identity
resolution, schema/governance, activation, and operational handoff.

## Why this exists

Every CDP engagement rediscovers the same questions — what to ask in discovery, how
to design identity resolution, what a good consent-enforcement design looks like,
what "done" means at each phase, what has to be in a handoff package. This captures
the answers once, as reusable templates and checklists, instead of re-deriving them
every time.

## Structure

- **`phases/`** — seven phases, Discovery through Handoff & Optimization. Each phase
  folder has a `README.md` (purpose, entry criteria, key activities, deliverables
  checklist, exit criteria, common pitfalls, look-ahead) and a `templates/` folder
  with the actual documents to copy and fill in.
- **`decision-log/`** — a lightweight ADR-style template for recording architecture
  decisions with rationale, used across all phases.
- **`risk-register/`** — a standard risk register template, used across all phases.
- **`diagrams/`** — guidance on which architecture diagrams matter at which phase,
  plus Mermaid starter templates (tool-agnostic — reproduce the same diagrams in
  Lucidchart, Visio, draw.io, whatever the engagement uses).
- **`glossary.md`** — cross-platform terminology map, so "datastream" (Adobe),
  "source" (Segment), "data source" (Tealium), "input" (mParticle), and "data
  stream" (Salesforce Data Cloud) are recognized as the same concept.

## Platform specialization

The methodology itself is vendor-agnostic. Where a template needs
platform-specific detail (e.g. XDM schema design is an Adobe AEP concept), the
template says so explicitly and gives the vendor-agnostic equivalent alongside
it (e.g. "canonical event/profile schema"). Add new platform call-outs as you
work other suites — don't fork the whole methodology per platform.

## The seven phases

| # | Phase | One-line purpose |
|---|---|---|
| 00 | [Discovery](phases/00-discovery/README.md) | Understand the client's current-state data landscape, stakeholders, and constraints. |
| 01 | [Strategy & Use Cases](phases/01-strategy-and-use-cases/README.md) | Define and prioritize the business use cases the CDP must serve. |
| 02 | [Design](phases/02-design/README.md) | Architect the target state: identity, schema, consent, integrations. |
| 03 | [Build & Configuration](phases/03-build-and-configuration/README.md) | Implement the design across environments. |
| 04 | [Validation & Testing](phases/04-validation-and-testing/README.md) | Prove the build matches the design and the data is trustworthy. |
| 05 | [Launch & Cutover](phases/05-launch-and-cutover/README.md) | Go live, safely, with a rollback plan. |
| 06 | [Handoff & Optimization](phases/06-handoff-and-optimization/README.md) | Transfer ownership and set up the post-launch operating model. |

Phases are usually sequential but not strictly gated — Design and Build often
overlap on real engagements, and Discovery findings can force a return to Strategy.
Treat the phase boundaries as checkpoints for "what should exist by now," not a
waterfall mandate.

Start with [`NAVIGATOR.md`](NAVIGATOR.md) for how to track and query engagement
progress against these phases.
