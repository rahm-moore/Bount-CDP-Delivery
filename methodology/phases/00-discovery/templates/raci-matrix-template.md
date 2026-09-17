# RACI Matrix Template

R = Responsible, A = Accountable, C = Consulted, I = Informed.

| Activity | Client Exec Sponsor | Client IT/Data Lead | Client Marketing Lead | Client Compliance | Architect (Bounteous) | Delivery Team (Bounteous) |
|---|---|---|---|---|---|---|
| Discovery findings sign-off | A | R | C | C | R | I |
| Use case prioritization | A | C | R | C | R | I |
| Target architecture design | I | A | C | C | R | C |
| Schema/identity design approval | I | A | I | C | R | C |
| Environment access provisioning | I | R/A | I | I | C | I |
| Build & configuration | I | C | I | I | A | R |
| Validation & testing sign-off | I | A | C | I | R | R |
| Go/no-go decision | A | R | C | C | C | I |
| Production cutover execution | I | C | I | I | A | R |
| Handoff acceptance | A | R | I | I | R | I |
| Post-launch governance ownership | I | A | I | I | C | I |

## Notes

- Exactly one **A** per row — accountability must be singular, even when
  responsibility is shared.
- Revisit this matrix at each phase transition; roles legitimately shift (e.g. IT
  is Accountable for build, but Marketing becomes Accountable for use-case-driven
  activation decisions).
- Add rows specific to the engagement's actual governance structure — this is a
  starting skeleton, not a fixed list.
