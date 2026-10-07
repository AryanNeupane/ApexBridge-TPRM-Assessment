# ApexBridge Technologies — TPRM Lifecycle Workflow

**Document Status:** Draft v0.1 — Simulated Project Artifact  
**Process Owner:** GRC Function  
**Applies To:** All third parties engaged by ApexBridge Technologies

---

## 1. Purpose

This workflow defines the end-to-end process ApexBridge Technologies uses to identify, assess, approve, monitor, and offboard third parties.

The workflow is designed to ensure that third-party risk is considered **before commitment**, assessed proportionally to the vendor's risk, and monitored throughout the relationship lifecycle.

---

## 2. Lifecycle Overview

The ApexBridge Technologies TPRM lifecycle consists of the following stages:

**Initiation → Screening → Tiering → Due Diligence → Assessment → Contract & Risk Requirements → Approval → Onboarding → Ongoing Monitoring → Periodic Reassessment → Renewal or Offboarding**

---

## 3. Lifecycle Stages

### 3.1 Initiation

The **Business Owner** submits a vendor request describing:

- Business need and purpose
- Candidate vendor(s)
- Services being provided
- Data involved
- Systems or applications involved
- Access required
- Expected duration of the relationship

The request provides the initial context required for TPRM screening and risk tiering.

---

### 3.2 Screening

**Procurement** logs the request and routes it through the GRC intake questionnaire.

The screening determines whether the proposed vendor:

- Handles company, customer, or employee data
- Connects to or accesses ApexBridge systems
- Creates a meaningful business dependency
- Provides a service that could materially affect business operations

#### Decision Point

**Does the vendor touch data, systems, or represent a meaningful business dependency?**

- **No →** Proceed through the light-touch path.
- **Yes →** Continue to risk tiering.

The purpose of screening is to determine the appropriate level of TPRM involvement before resources are committed to detailed due diligence.

---

### 3.3 Risk Tiering

**GRC** assigns a preliminary risk tier based on factors including:

- Data sensitivity
- Level of system or privileged access
- Business criticality
- Operational dependency
- Potential impact if the vendor becomes unavailable or compromised

The preliminary tier is classified as:

- **Low**
- **Medium**
- **High**

The tier determines the depth of due diligence, assessment requirements, approval authority, and reassessment frequency.

---

### 3.4 Due Diligence

**GRC and Information Security** collect evidence appropriate to the vendor's assigned tier.

Depending on the risk level, evidence may include:

- Security questionnaire
- SOC 2 report
- ISO/IEC 27001 certification
- Information security policies
- Business continuity / disaster recovery information
- Vulnerability management information
- Incident response documentation
- Financial stability information
- Business references

Higher-risk vendors receive deeper due diligence and evidence review.

The objective is to move beyond vendor assertions and determine whether the vendor can provide sufficient evidence to support its stated controls and capabilities.

---

### 3.5 Risk Assessment

**GRC**, with support from **Information Security and Privacy where required**, evaluates the collected evidence against ApexBridge's third-party risk criteria.

The assessment produces:

- Risk rating
- Key findings
- Control gaps
- Residual risk considerations
- Recommended treatment
- Risk acceptance recommendation

#### Decision Point

**Is the identified risk acceptable at the proposed tier?**

**Yes →** Proceed to contracting.

**Treatable →** Initiate remediation and/or exception process, then proceed to contracting once the required decision or conditions are documented.

**No →** Reject the vendor or seek an alternative solution.

---

### 3.6 Contract & Risk Requirements

**Legal** incorporates applicable risk requirements into the vendor agreement.

Depending on the relationship and risk level, contractual requirements may include:

- Information security requirements
- Data Processing Agreement (DPA)
- Data protection obligations
- Audit and assessment rights
- Breach notification requirements
- Security incident notification
- Confidentiality requirements
- Subcontractor requirements
- Business continuity requirements
- Termination rights
- Data return and destruction requirements

Contract requirements should reflect the risks identified during the assessment rather than being treated as a separate process.

---

### 3.7 Approval

Formal risk acceptance is recorded by the authority appropriate to the vendor's risk tier.

| Risk Level / Decision | Approval Authority |
|---|---|
| Low | GRC |
| Medium | GRC under delegated authority |
| High | Executive Management |
| Material Exception | Executive Management |

The approval record should document:

- Vendor
- Risk tier
- Key risks
- Residual risk
- Required controls or conditions
- Exception details, if applicable
- Decision
- Approver
- Approval date

---

### 3.8 Onboarding

Once approval and contractual requirements are complete, the vendor proceeds to onboarding.

**IT / Engineering** provisions access strictly according to the approved scope.

**GRC** creates or updates the vendor record, including:

- Vendor name
- Business Owner
- Service provided
- Risk tier
- Data classification
- Systems accessed
- Approval status
- Contract information
- Key risk findings
- Exception status
- Next reassessment date

Access must not exceed the scope approved during the TPRM process.

---

### 3.9 Ongoing Monitoring

TPRM does not end when a vendor is onboarded.

The **Business Owner** monitors business performance and service-level obligations.

**GRC and Information Security** monitor for:

- Security incidents
- Material control changes
- Significant changes in service scope
- Changes in data handled
- Changes in system access
- Significant vendor ownership changes
- Expired certifications
- Material negative events
- Significant changes in business criticality

Material changes may trigger an **off-cycle reassessment** rather than waiting for the next scheduled review.

---

### 3.10 Periodic Reassessment

GRC reassesses vendors according to their risk tier.

| Risk Tier | Baseline Reassessment Cadence |
|---|---|
| **High** | Annual |
| **Medium** | Biennial |
| **Low** | Ad hoc, based on material change or risk trigger |

The reassessment should consider whether the original risk assumptions remain valid.

Triggers for an earlier reassessment may include:

- Security incident
- Major control failure
- Significant change in data processing
- New system or privileged access
- Material change in business dependency
- Expired assurance evidence
- Significant vendor organizational change
- Regulatory or contractual change

---

### 3.11 Renewal or Offboarding

At contract renewal, the vendor record and risk tier are revisited to determine whether:

- The service scope has changed
- Data handled has changed
- Access requirements have changed
- Business criticality has changed
- New risks have emerged
- Existing evidence remains current
- A new assessment is required

If the relationship ends:

1. IT revokes vendor access.
2. Business Owner confirms services have ended.
3. Data return or destruction is confirmed where applicable.
4. Outstanding contractual obligations are addressed.
5. Open risks or exceptions are closed or transferred.
6. The vendor record is formally closed.

---

## 4. Lifecycle Decision Logic

The core decision logic can be summarized as:

```text
Business Need
      ↓
Vendor Identification
      ↓
Initial Screening
      ↓
Does the vendor touch data, systems,
or create meaningful dependency?
      ├── No → Light-Touch Path
      │
      └── Yes
           ↓
      Risk Tiering
           ↓
      Due Diligence
           ↓
      Risk Assessment
           ↓
      Is Risk Acceptable?
        ├── Yes → Contracting
        │
        ├── Treatable
        │      ↓
        │   Remediation /
        │   Exception
        │      ↓
        │   Contracting
        │
        └── No → Reject / Seek Alternative