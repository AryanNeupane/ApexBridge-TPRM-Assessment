

````markdown
# ApexBridge Technologies | Third-Party Risk Management

A practical, simulated Third-Party Risk Management (TPRM) programme built to demonstrate how a GRC function can identify, assess, treat, monitor, and report third-party risk across the vendor lifecycle.

> **Project Type:** Simulated GRC / TPRM Portfolio Project  
> **Role:** GRC Analyst  
> **Organization:** ApexBridge Technologies  
> **Vendor Population:** 47 third parties  
> **Detailed Assessments:** 6 vendors  
> **Primary Focus:** Third-Party Risk, Security Assurance, Evidence Review, Risk Treatment, Monitoring

---

## Overview

Third-party risk management is not simply sending vendors a security questionnaire and recording their answers.

A useful TPRM programme needs to answer:

- Which third parties does the organization depend on?
- Which vendors represent the greatest risk?
- What data and systems can they access?
- What evidence supports their control environment?
- Which risks require remediation or management acceptance?
- What happens when the vendor's risk profile changes?

This project was built around those questions.

The simulated ApexBridge programme covers the lifecycle from vendor governance and inventory through assessment, evidence review, remediation, risk acceptance, monitoring, reassessment, and management reporting.

---

## TPRM Lifecycle

```text
Govern
   ↓
Inventory
   ↓
Tier
   ↓
Assess
   ↓
Evidence Review
   ↓
Remediate / Accept / Transfer / Avoid
   ↓
Monitor
   ↓
Report
   ↓
Reassess on Change
````

The goal is to demonstrate a lifecycle rather than a collection of disconnected vendor spreadsheets.

---

# Project Context

ApexBridge Technologies is a fictional B2B SaaS and digital services organization with approximately 300 employees.

The organization relies on third parties for:

* Cloud infrastructure
* Software development and CI/CD
* Payment processing
* Security services
* HR and payroll
* Data analytics
* Customer support
* Marketing
* Business operations

The simulated vendor population contains **47 third parties**.

### Vendor Population

| Tier      | Vendors | General Profile                                                    |
| --------- | ------- | ------------------------------------------------------------------ |
| Tier 1    | 6       | Critical services, sensitive data, production or privileged access |
| Tier 2    | 11      | Significant business or security dependency                        |
| Tier 3    | 18      | Lower-risk business services                                       |
| Tier 4    | 12      | Minimal security or data exposure                                  |
| **Total** | **47**  |                                                                    |

---

# What Was Built

The project includes practical TPRM artefacts covering the full lifecycle.

```text
ApexBridge-TPRM/
│
├── 01-Governance/
│   ├── TPRM Governance & Operating Model
│   ├── TPRM Lifecycle Workflow
│   └── TPRM RACI
│
├── 02-Vendor-Inventory/
│   └── Vendor Inventory
│
├── 03-Tiering/
│   └── Vendor Tiering Methodology
│
├── 04-Assessment/
│   ├── Due Diligence Requirements Matrix
│   ├── Vendor Risk Assessment
│   └── Assessment Summary
│
├── 05-Evidence-Review/
│   ├── Evidence Review Methodology
│   └── Evidence Review Workbook
│
├── 06-Findings/
│   └── Vendor Findings & Observations Register
│
├── 07-Remediation/
│   ├── Remediation & Risk Treatment Tracker
│   └── Remediation & Risk Treatment Methodology
│
├── 08-Risk-Acceptance/
│   └── RA-001 NorthPeak
│
├── 09-Monitoring/
│   ├── Monitoring Dataset
│   ├── Monitoring & Reassessment Schedule
│   └── TPRM Trigger Matrix
│
├── 10-Reporting/
│   └── TPRM Management Report
│
└── README.md
```

---

# Assessment Scope

Six vendors were assessed in depth during the initial cycle.

| Vendor           | Tier    | Service                         | Key Risk Area                         |
| ---------------- | ------- | ------------------------------- | ------------------------------------- |
| NorthPeak        | T1      | Production cloud infrastructure | Assurance scope                       |
| Corestack        | T1      | CI/CD and deployment            | Privileged production access          |
| Guardline        | T2      | Managed security services       | Evidence currency                     |
| Meridian Pay     | T2      | Payment processing              | Subprocessor assurance                |
| Ferrow Analytics | Pending | Data analytics                  | Data access and incomplete assessment |
| Brightloop       | T3      | Marketing automation            | Proportionality / low exposure        |

The project also contains additional vendors in the monitoring dataset to demonstrate how TPRM continues beyond the initial assessment.

---

# Key Programme Metrics

The initial cycle produced the following simulated portfolio view:

| Metric                           | Result  |
| -------------------------------- | ------- |
| Total third parties              | 47      |
| Tier 1 vendors                   | 6       |
| Tier 2 vendors                   | 11      |
| Tier 3 vendors                   | 18      |
| Tier 4 vendors                   | 12      |
| Current risk assessment coverage | 31 / 47 |
| Assessment coverage              | 66%     |
| T1 current assessment coverage   | 5 / 6   |
| Required evidence current        | 15 / 17 |
| Open findings                    | 5       |
| Overdue findings                 | 2       |
| Active risk acceptances          | 1       |
| Detailed vendors assessed        | 6       |
| Evidence items reviewed          | 11      |

The limitations in these metrics are intentionally visible rather than hidden.

---

# Key Findings

## F-002 | Corestack

**Severity:** High

Corestack provides CI/CD and production deployment capabilities.

The assessment identified privileged production deployment access without adequate managed secrets management.

### Risk

Poorly controlled production credentials could enable unauthorized or insufficiently governed deployment activity.

### Treatment

**Mitigate**

Actions include:

* Managed secrets storage
* Credential rotation
* Scoped service account
* Approval-gated promotion
* Interim permission restrictions
* Deployment alerting

The vendor remediation subsequently became overdue.

Rather than treating the missed date as an administrative issue, the monitoring process evaluated whether the interim control remained effective and escalated the treatment decision.

---

## F-006 | Corestack

**Severity:** Medium

Available penetration testing evidence was 26 months old and predated a major platform release.

The issue is tracked separately from F-002 because the risk and corrective action are different.

### Treatment

**Mitigate**

Required action:

* Obtain current penetration testing
* Confirm relevant production scope
* Review high-severity findings
* Validate remediation or documented risk treatment

---

## F-001 | NorthPeak

**Severity:** Medium

NorthPeak hosts ApexBridge's production environment.

The available SOC 2 report has a scope limitation around logical access, with relevant controls identified as complementary user entity controls.

The assessment did not automatically treat this as a failed vendor control.

Instead, it considered:

* SOC 2 scope
* ISO 27001 certification scope
* Complementary User Entity Controls
* ApexBridge tenant-level IAM controls
* Production criticality
* Vendor replaceability
* Business continuity considerations

### Treatment

**Risk Accepted with Conditions**

The risk acceptance record documents:

* Risk owner
* Approver
* Business context
* Inherent risk
* Existing controls
* Residual risk
* Rationale
* Alternatives considered
* Conditions
* Review date
* Reassessment triggers

The risk is **accepted, not closed**.

---

## F-003 | Meridian Pay

**Severity:** Medium

Meridian Pay disclosed a new payment subprocessor involved in fraud screening.

The issue is treated as a fourth-party assurance and contractual visibility concern.

Tokenization reduces direct card-data exposure, but does not eliminate the need to understand the subprocessor.

### Treatment

**Mitigate + Transfer / Share**

Actions include:

* Obtain processor assurance
* Review subprocessor information
* Confirm contractual notification requirements
* Confirm pass-through obligations
* Track the issue through remediation

---

## F-005 | Ferrow Analytics

**Severity:** Medium

Ferrow Analytics has access to raw customer data, but the assessment is incomplete.

Approximately 60% of the questionnaire has been completed.

The key problem is not simply an incomplete questionnaire.

ApexBridge does not yet have enough information to confidently establish:

* Final risk tier
* Data-processing scope
* Access requirements
* Retention requirements
* Subcontractor exposure
* Appropriate monitoring baseline

The vendor therefore remains an identified risk information gap rather than being assumed to be low risk.

---

## F-004 | Guardline

**Severity:** Low

Guardline's assurance evidence was renewed on time, but ApexBridge lacked a reliable mechanism for tracking evidence expiry.

The issue is therefore primarily an internal TPRM process weakness.

### Treatment

**Mitigate**

Actions include:

* Record evidence expiry dates
* Establish pre-expiry alerts
* Monitor T1 and T2 assurance currency
* Prevent evidence from silently becoming stale

---

## OBS-01 | Brightloop

**Classification:** Observation

Brightloop has:

* No system access
* No production access
* No sensitive production data
* Limited prospect contact information

The available public trust information provides a reasonable baseline for the current risk.

No formal remediation was required.

The observation remains documented to demonstrate proportionality.

Not every vendor issue should become a formal finding.

---

# Evidence Review Approach

The project uses an evidence-based assessment methodology.

Evidence is evaluated for:

* Relevance
* Scope
* Validity
* Currency
* Completeness
* Reliability

### Evidence Reliability

| Level  | Evidence Type                               | General Strength |
| ------ | ------------------------------------------- | ---------------- |
| Tier 1 | Independent assurance / third-party testing | Highest          |
| Tier 2 | Internal operational evidence               | Moderate         |
| Tier 3 | Policy / procedure                          | Design evidence  |
| Tier 4 | Self-attestation / unsupported statement    | Lowest           |

A major principle in the project is:

> Evidence reliability is not the same as evidence sufficiency.

A highly reliable report can still be insufficient if it does not cover the relevant service, system, control, location, or assessment period.

---

# Risk Treatment

The project uses four primary treatment options:

```text
Mitigate
Accept
Avoid
Transfer / Share
```

Treatment decisions consider:

* Risk severity
* Business criticality
* Data sensitivity
* System access
* Existing controls
* Compensating controls
* Vendor replaceability
* Cost and feasibility
* Regulatory considerations
* Residual risk
* Management authority

---

# Risk Acceptance

Risk acceptance is used when management decides that the remaining risk is understood and tolerable under defined conditions.

The project includes a formal acceptance record for NorthPeak.

The record includes:

* Risk
* Business context
* Inherent risk
* Existing controls
* Residual risk
* Rationale
* Alternatives considered
* Risk owner
* Approver
* Acceptance date
* Review date
* Conditions
* Monitoring requirements
* Reassessment triggers

The key principle is:

> Risk acceptance is a decision, not a closure mechanism.

---

# Remediation & Closure

Findings are not considered closed simply because a vendor says the issue has been fixed.

The closure process is:

```text
Action Implemented
       ↓
Evidence Submitted
       ↓
GRC Validation
       ↓
Effectiveness Confirmed
       ↓
Closure Approved
```

Evidence is evaluated for:

* Scope
* Currency
* Relevance
* Completeness
* Effectiveness

This creates a distinction between **remediation activity** and **validated risk reduction**.

---

# Compensating Controls

Where remediation cannot be completed immediately, temporary compensating controls may be used.

For Corestack F-002, interim measures include:

* Restricted permissions
* Scoped service accounts
* Approval-gated deployment
* Deployment monitoring

These controls reduce exposure while the primary remediation remains outstanding.

They do not permanently replace the required remediation.

If the remediation continues to slip, the issue becomes a treatment and escalation decision rather than simply a scheduling problem.

---

# Monitoring

TPRM does not end when the initial assessment is completed.

The monitoring model uses different cadences based on risk.

| Tier   | Typical Monitoring               |
| ------ | -------------------------------- |
| Tier 1 | Quarterly + annual reassessment  |
| Tier 2 | Semiannual + annual reassessment |
| Tier 3 | Annual review                    |
| Tier 4 | Trigger-based                    |

Monitoring includes:

* Security incidents
* Certification status
* Evidence expiry
* Open remediation
* Subprocessor changes
* Access changes
* Data scope changes
* Service changes
* Business criticality
* Business continuity concerns

---

# Reassessment Triggers

A vendor is reassessed when a material change can invalidate the original risk assessment.

Examples include:

### Security Incident

```text
Incident
   ↓
Obtain details
   ↓
Assess impact
   ↓
Increase monitoring
   ↓
Priority reassessment
   ↓
Escalation if required
```

### New Subprocessor

```text
New subprocessor
   ↓
Identify service and data exposure
   ↓
Review assurance
   ↓
Assess fourth-party risk
   ↓
Scoped reassessment
```

### Expanded Access

A change from limited application access to SSO, privileged access, production access, or sensitive data access may require re-tiering and reassessment.

Other triggers include:

* Expired assurance
* Loss of certification
* High-risk remediation becoming overdue
* Criticality increase
* Acceptance condition breach
* Material architecture change
* M&A activity
* Financial instability
* Changes to data-processing terms

---

# Management Reporting

The project includes a management report designed to convert operational TPRM data into decision-useful information.

The initial cycle identified five major themes:

### 1. Assurance Evidence Ageing

Two Tier 1 vendors currently lack the level of current independent assurance desired for full risk closure.

### 2. Critical Vendor Concentration

NorthPeak supports the production environment while Corestack is embedded in the deployment path.

This represents structural dependency and business continuity exposure.

It is not automatically a vendor control failure.

### 3. Remediation Delivery

Corestack F-002 is overdue.

The issue demonstrates why monitoring needs to evaluate actual remediation progress rather than simply record target dates.

### 4. Subprocessor Visibility

Meridian Pay disclosed a new subprocessor.

The TPRM process must therefore account for fourth-party exposure rather than stopping at the direct vendor.

### 5. Incomplete Risk Data

Ferrow Analytics has raw customer data access while its assessment and tiering remain incomplete.

Uncertainty itself needs to be managed.

---

# Management Attention

The management report identifies specific decisions requiring attention.

### Solvane

A Tier 1 payroll vendor has:

* An active security incident
* An expired ISO 27001 certification
* An overdue reassessment

This requires priority reassessment and heightened monitoring.

### Corestack

F-002 is a High finding with overdue remediation.

Management must decide whether the revised remediation commitment is acceptable under controlled interim conditions.

### NorthPeak

The current risk acceptance has an outstanding condition.

CUEC verification needs to be completed within the defined timeframe or the acceptance should be reconsidered.

### Portfolio Coverage

Current detailed assessment coverage is 66%.

The next assessment wave should prioritize remaining Tier 1 and Tier 2 vendors.

---

# Key GRC Principles Demonstrated

## A questionnaire is an input, not the assessment

A questionnaire provides vendor information.

The assessment requires judgment across:

```text
Business Context
      +
Risk Exposure
      +
Existing Controls
      +
Evidence
      +
Control Gaps
      +
Residual Risk
      =
Risk Decision
```

## Certifications are not automatic proof of sufficiency

A vendor having ISO 27001 or SOC 2 does not automatically mean every relevant control has been independently evidenced.

Scope matters.

## Accepted does not mean closed

An accepted risk still requires:

* Ownership
* Conditions
* Review date
* Monitoring
* Reassessment triggers

## Findings need evidence

A control gap should be supported by evidence.

Root cause should not be invented where evidence is insufficient.

## Monitoring is part of the lifecycle

Vendor risk can change because of:

* Incidents
* New subprocessors
* New access
* Expired assurance
* Business changes
* Architecture changes
* Remediation failure

Therefore, TPRM must continue after the initial assessment.

---

# Framework Alignment

The project draws on concepts from:

* ISO/IEC 27001
* ISO/IEC 27001 risk management concepts
* NIST Cybersecurity Framework
* Third-party risk management practices
* Security assurance and audit principles

The project does **not** claim formal certification or compliance for ApexBridge Technologies.

---

# What This Project Demonstrates

This project demonstrates practical ability to:

* Build a TPRM operating model
* Create a vendor inventory
* Apply risk-based vendor tiering
* Define due diligence requirements
* Assess vendor security risk
* Review security evidence
* Identify evidence gaps
* Distinguish control gaps from evidence gaps
* Assign risk severity
* Recommend risk treatment
* Track remediation
* Use compensating controls
* Document risk acceptance
* Define monitoring requirements
* Establish reassessment triggers
* Escalate material issues
* Produce management reporting

More importantly, the project demonstrates the reasoning behind those activities rather than simply producing templates.

---

# Portfolio Limitations

This is a simulated portfolio project.

The following are fictional:

* ApexBridge Technologies
* Vendors
* Employees
* Systems
* Contracts
* Evidence
* Findings
* Risk ratings
* Metrics
* Management decisions

The project does not represent confidential employer or client work.

No production security implementation or external vendor assessment is being claimed.

The data is intentionally imperfect in places to demonstrate how a GRC analyst handles uncertainty, incomplete evidence, overdue remediation, and changing vendor risk.

---

# Interview Discussion

The project can be defended through questions such as:

### Why isn't a questionnaire enough?

Because a questionnaire records vendor responses, but it does not independently establish whether controls are appropriate, operating, current, or relevant to the assessed service.

### Why was NorthPeak accepted instead of closed?

Because the SOC 2 limitation created an assurance gap, but other assurance and ApexBridge controls reduced the residual risk to a level management could accept.

### Why is the NorthPeak finding not closed?

Because risk acceptance does not remove the underlying risk. The risk remains subject to conditions, monitoring, and reassessment.

### Why did Corestack receive more frequent monitoring?

Because it has an open High finding involving privileged production deployment access.

### Why wasn't every vendor assessed in depth?

Because TPRM should be risk-based. Critical and higher-risk vendors require deeper assessment and more frequent monitoring.

### Why does Ferrow matter if the questionnaire is incomplete?

Because the vendor has raw customer data access. The absence of sufficient information prevents ApexBridge from confidently determining its risk position.

### Why does a new subprocessor matter?

Because the direct vendor may introduce another organization into the service or data chain, creating additional security, contractual, privacy, and concentration considerations.

---

# Final Takeaway

The central lesson from this project is that TPRM is not a one-time questionnaire exercise.

A mature process connects:

```text
Vendor Dependency
      ↓
Risk Tier
      ↓
Assessment
      ↓
Evidence
      ↓
Findings
      ↓
Treatment
      ↓
Validation
      ↓
Monitoring
      ↓
Reassessment
      ↓
Management Decision
```

The purpose of the programme is not to make every vendor look "compliant."

The purpose is to make the organization's third-party risk position understandable, defensible, and actionable.

---

## Disclaimer

**ApexBridge Technologies is a fictional organization created for portfolio development.**

All organizations, vendors, systems, evidence, findings, risk ratings, metrics, and scenarios in this repository are simulated.

This project is intended to demonstrate practical GRC and TPRM knowledge for portfolio and interview purposes.


