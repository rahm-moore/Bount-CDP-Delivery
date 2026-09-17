# Use Case Prioritization Matrix

| Use Case | Business Value (1-5) | Feasibility (1-5) | Data Readiness (1-5) | Effort (S/M/L/XL) | Priority Score* | Business Owner | Target Release |
|---|---|---|---|---|---|---|---|
| | | | | | | | |

\* Suggested scoring: `Priority Score = (Business Value + Feasibility + Data Readiness) / Effort-weight`,
where Effort-weight is S=1, M=2, L=3, XL=5. Adjust the formula to match the
engagement's actual decision-making style — the point is a *consistent, explainable*
method, not a specific formula.

## Scoring guidance

- **Business Value** — revenue impact, cost savings, risk reduction, or strategic
  importance, as scored by the business owner, not the architect.
- **Feasibility** — technical feasibility given current platform capabilities and
  team skill, as scored by the architect/delivery team.
- **Data Readiness** — pull directly from the Discovery source inventory's data
  quality notes. A use case needing data flagged "poor quality" or "access denied"
  should score low here regardless of business value.
- **Effort** — rough sizing, not a committed estimate; refine once the use case
  reaches Design.

## Output

Sort by Priority Score, then sequence into releases with the sponsor. Feed the
top-tier use cases into
[`business-case-template.md`](business-case-template.md).
