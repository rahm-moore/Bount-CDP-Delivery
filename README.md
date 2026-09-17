# Bounteous CDP Delivery

This repo is the Architect's working library for **Customer Data Platform (CDP)
implementation delivery** — everything an Architect produces or references from
Discovery through Handoff, on any engagement.

## What's in here

| Path | Purpose |
|---|---|
| [`methodology/`](methodology/) | **The Data Systems Architect Bible.** A vendor-agnostic, phase-by-phase CDP implementation methodology with entry/exit criteria, deliverables checklists, and best-practice templates (docs, diagrams, decision logs, risk registers). Reusable across every engagement and every platform (Adobe AEP/RTCDP, Segment, Tealium, mParticle, Salesforce Data Cloud, etc.). Adobe-specific guidance is layered in explicitly, not assumed. |
| [`engagements/`](engagements/) | One folder per active client engagement. Each holds a `STATUS.md` tracking real progress against the methodology's phases (so you can say "here's where we are" and get next steps), plus engagement-specific deliverables. |
| `aep-promotion-form.html` | Standalone delivery tool: AEP/RTCDP promotion request form. |

## How to use this repo

1. **Starting a new engagement?** Copy `engagements/_TEMPLATE/` to `engagements/<client-name>/`
   and fill in `STATUS.md`.
2. **Mid-engagement, need to know what's next?** Open the engagement's `STATUS.md`, find the
   current phase, then open that phase's `README.md` under `methodology/phases/` — its "Exit
   Criteria" and "Look Ahead" sections tell you what's left and what's coming.
3. **Need a template** (RACI matrix, XDM/schema design doc, go-live runbook, handoff checklist,
   decision log, risk register, architecture diagram)? It's under the current phase's
   `templates/` folder in `methodology/`.
4. **Building out the methodology itself?** Add or refine templates in place; update the phase
   `README.md`'s deliverables checklist to reference anything new.

See [`methodology/README.md`](methodology/README.md) for the full methodology overview and
[`methodology/NAVIGATOR.md`](methodology/NAVIGATOR.md) for the phase map and how the
"where am I / what's next" workflow works in detail.
