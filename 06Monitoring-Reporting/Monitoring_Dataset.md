# ApexBridge Monitoring Dataset

Ten vendors from the population carried through the project.

The data is deliberately imperfect. Reasoning about it is the exercise.

| Vendor | Tier | Business / Risk Owner | Service | Data & Access | Last Assessed | Next Review | Assurance Status | Evidence Expiry | Open / Overdue Findings | Acceptance | Material Changes |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **Guardline** | T2 | CISO | Managed SOC monitoring | Security telemetry; partial prod visibility | Current cycle | +12 mo | ISO 27001 current | +29 mo | F-004 open (Low, ApexBridge-owned) | — | None reported |
| **Corestack** | T1 | VP Engineering | CI/CD pipeline | Privileged prod repo access | Current cycle | +12 mo | None independent | n/a | F-002 **overdue 12d**; F-006 **overdue 5d** | — | Vendor fix slipped past agreed date |
| **Solvane HR & Payroll** | T1 | Head of People | Payroll & benefits | Employee PII, banking detail | 14 months ago | **Overdue** | ISO 27001 **expired** | −6 weeks | None recorded | — | **Security incident notified** |
| **NorthPeak** | T1 | VP Engineering | Production cloud hosting | Customer + employee data; full prod | Current cycle | +12 mo | SOC 2 (scope-limited) + ISO current | +15 mo | F-001 accepted | RA-001 active, review in 3 mo | CUEC verification condition **overdue** |
| **Meridian Pay** | T2 | Finance Director | Payment gateway | Tokenised payment data; API | Current cycle | +12 mo | Self-attestation (SAQ) | +8 mo | F-003 open, on plan | — | **New subprocessor announced** (fraud screening) |
| **HelpDeskly** | T2 | Head of Customer Success | Support ticketing | Customer contact + support content | Current cycle | +12 mo | SOC 2 Type II current | +10 mo | None | — | None reported |
| **PulseSurvey** | T2 (pending) | Head of People | Employee engagement surveys | Employee PII; **SSO now confirmed** | Current cycle | +12 mo | None requested | n/a | None | — | **Criticality increased**; now the sole tool for a board-reported engagement programme |
| **Ferrow Analytics** | **Unassigned** | Dir. Product Analytics | Data analytics contracting | Raw customer dataset; scope unclear | Never completed | **Undefined** | Partial questionnaire (60%) | n/a | F-005 awaiting vendor, due in 18d | — | **Monitoring data incomplete** |
| **Brightloop** | T3 | Marketing Director | Marketing automation | Prospect contact data; no system access | Current cycle | +24 mo | Public trust page | n/a | OBS-01 closed | — | None reported |
| **CrestOffice Supplies** | T4 | Office Manager | Office consumables | None | Tiering only | Trigger-based | Not required |  |  |  |  |

## Dataset Notes

- The dataset contains both vendor-owned and ApexBridge-owned issues.
- Some vendors have material changes that should trigger reassessment outside the normal review cadence.
- Overdue reviews, expired assurance, overdue acceptance conditions, and overdue remediation should not be treated as equivalent conditions.
- Tier status can change when business criticality, data access, or service scope changes.
- Absence of an open finding does not necessarily mean the vendor presents no current risk.
- Monitoring is intended to identify changes that may require reassessment, not simply to maintain a static vendor register.