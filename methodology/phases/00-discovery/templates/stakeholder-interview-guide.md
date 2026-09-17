# Stakeholder Interview Guide

Use one pass per stakeholder group. Adapt questions to context — the goal is
surfacing facts and pain points, not filling out every line item.

## Business / Marketing stakeholders

- What decisions do you make today using customer data? What data do you wish you had?
- What campaigns or personalization efforts are blocked or degraded by current data gaps?
- Who "owns" the customer data strategy today, if anyone?
- What does success look like for this CDP initiative, in your own words?
- What's the single most painful manual process involving customer data today?

## IT / Data Engineering stakeholders

- Walk me through how an event (e.g. a page view, a form submit, a transaction)
  actually gets from the source system to wherever it's reported today.
- What systems have you inherited that nobody fully understands anymore?
- What's your current environment/promotion process (dev → staging → prod)?
- What's broken or fragile that you already know about but haven't had time to fix?
- Who has admin access to [CDP platform], and is that access list accurate?

## Compliance / Legal / Privacy stakeholders

- What consent management platform is in use, and what categories does it define?
- Is consent enforcement independently verified today, or trusted by default?
- Are there jurisdiction-specific requirements in scope (GDPR, CCPA/CPRA, GLBA, HIPAA, etc.)?
- Has a data subject access/deletion request ever been tested end-to-end?
- Are there known PII-handling issues (e.g. reversible "hashes," plaintext PII in
  unexpected fields) already on record?

## Executive sponsor

- What's the business case that got this funded? What's the ROI expectation and timeline?
- What would make this project a failure in your eyes, even if it's technically delivered?
- Who needs to say yes at each major gate (design sign-off, go-live)?

## Output

Notes from each interview feed the Discovery findings summary and the candidate
use-case list (captured, not prioritized — that's Phase 01).
