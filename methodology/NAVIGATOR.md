# Navigator — "Where am I, and what's next?"

This is the mechanism for turning "here's my current phase" into "here's exactly
what to do next." It works whether you're reading this yourself or asking a Claude
Code session that has this repo open.

## The workflow

1. **Every engagement has a `STATUS.md`** at `engagements/<client>/STATUS.md`
   (instantiated from [`engagements/_TEMPLATE/STATUS.md`](../engagements/_TEMPLATE/STATUS.md)).
   It records the current phase and a checklist of which phase deliverables are
   done, in progress, or not started.
2. **To ask "what's next":** open that engagement's `STATUS.md`, find the current
   phase, then open `methodology/phases/<phase>/README.md` for that phase. Read,
   in order:
   - **Deliverables checklist** — cross-reference against `STATUS.md` to see
     what's still open for *this* phase.
   - **Exit Criteria** — what must be true before moving to the next phase.
   - **Look Ahead** — what the *next* phase will need from you, so you can start
     collecting it now instead of hitting a cold start later.
3. **When a phase's exit criteria are met**, update `STATUS.md`'s current phase
   and re-run the check against the new phase's README.

If you're asking a Claude Code session this question directly ("where should I
focus next on the Acme engagement?"), point it at the engagement's `STATUS.md` —
it can do steps 2–3 itself and report back a concrete next-steps list rather than
a generic phase description.

## Phase map (quick reference)

| # | Phase | Typical trigger to enter | Typical trigger to exit |
|---|---|---|---|
| 00 | Discovery | Engagement kicked off, no current-state documentation exists yet | Current-state architecture, stakeholder map, and source inventory are documented and validated with the client |
| 01 | Strategy & Use Cases | Current state understood | Prioritized use case list is signed off, with a business case per use case |
| 02 | Design | Use cases prioritized | Target architecture (identity, schema, consent, integrations) is designed and reviewed |
| 03 | Build & Configuration | Design approved | Build matches the design in at least one non-prod environment |
| 04 | Validation & Testing | Build exists | Data quality, identity resolution, and consent enforcement are all validated against defined acceptance criteria |
| 05 | Launch & Cutover | Validation passed, go/no-go given | Production is live, stable, and the rollback window has passed |
| 06 | Handoff & Optimization | Production stable | Client owns operations; a post-launch roadmap exists |

## Non-linearity is normal

A finding in Validation & Testing (04) that reveals a Design (02) gap doesn't mean
starting over — it means: fix the Design doc, note the change in the
[decision log](../decision-log/decision-log-template.md), assess Build impact, and
continue. Update `STATUS.md` to reflect the phase you're *actually* working in, even
if that means stepping back one.

## Multi-platform note

The phase map and "what's next" logic don't change by platform. What changes is
*which templates* apply inside a phase (e.g. Design's schema template has an Adobe
XDM variant and a generic canonical-schema variant — see
[`glossary.md`](glossary.md) for the term mapping). `STATUS.md` records which
platform an engagement uses so the right template variant is obvious.
