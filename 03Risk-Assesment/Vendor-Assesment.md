# ApexBridge Technologies — Vendor Assessment Findings & Recommended Actions

**Document Status:** Draft v0.1  
**Document Owner:** GRC Function  
**Assessment Type:** Third-Party Risk Assessment  
**Project Context:** Simulated TPRM Project  

## Assessment Approach

The assessment does not treat the presence of a document as proof that a control is effective. Each vendor was evaluated based on:

- What was actually observed
- Why the observation matters to ApexBridge
- What evidence supports the observation
- What remains uncertain
- The resulting risk implication
- The recommended action

The reasoning is the deliverable, not simply the final risk label.

---

## 1. NorthPeak Cloud Infrastructure

**Tier:** Tier 1  
**Service:** Cloud hosting for production environment  
**Owner:** VP Engineering  

### Observed

A current SOC 2 Type II report exists, but its system boundary appears primarily focused on physical and environmental controls at the data-center level.

### Why It Matters

NorthPeak has full production access and hosts ApexBridge's core environment. The primary concern is therefore logical and application-layer access, not simply physical security of the underlying data center.

A current assurance report is useful only to the extent that its scope covers the controls relevant to ApexBridge's actual risk exposure.

### Evidence Supporting the Observation

- Current SOC 2 Type II report
- Review of the report's stated system boundary and scope language
- Existing commercial contract containing a general security clause

### Remaining Uncertainty

It is not yet clear whether NorthPeak maintains separate evidence covering:

- Application-layer access controls
- Logical privileged-access controls
- Production environment access management
- Related identity and access-management controls

This evidence may exist but was not provided as part of the current assessment package.

### Risk Implication

Residual risk remains elevated relative to what the presence of the SOC 2 report might initially suggest.

The report provides some assurance, but it does not clearly address the specific control area ApexBridge is most concerned about. The issue is therefore not that the SOC 2 report is invalid; it is that its scope may not sufficiently cover the relevant risk.

### Recommended Action

**Request Additional Evidence**

Request evidence specifically addressing logical and application-layer access controls, or confirmation of an assurance report whose scope includes those controls.

NorthPeak should not be treated as fully closed until the scope gap is resolved.

---

## 2. Corestack DevOps Tooling

**Tier:** Tier 1  
**Service:** CI/CD pipeline with privileged production repository access  
**Owner:** VP Engineering  

### Observed

Corestack has no independent assurance on file. The primary evidence is a completed ApexBridge security questionnaire, including a vague statement that secrets are managed using "industry-standard practices."

### Why It Matters

Corestack has privileged access to production repositories and deployment infrastructure.

This creates significant supply-chain and production security exposure. A general statement about security practices is insufficient to demonstrate that secrets are actually protected through an effective and controlled process.

### Evidence Supporting the Observation

- Completed ApexBridge security questionnaire
- Vendor response describing general security practices

The questionnaire response is currently a claim rather than independently verified evidence.

### Remaining Uncertainty

It remains unclear whether Corestack:

- Uses a defined secrets-management platform
- Has documented secrets-management procedures
- Performs appropriate access reviews
- Has independent security testing
- Has identified and remediated relevant CI/CD security risks

The underlying control environment may be mature, but ApexBridge currently has insufficient evidence to establish that.

### Risk Implication

Residual risk remains close to inherent risk because very little has been independently verified.

The combination of privileged production access and weak assurance makes this one of the more significant evidence gaps in the current vendor population.

### Recommended Action

**Require Remediation**

Request specific evidence covering secrets management and privileged access controls.

At minimum, this should identify the actual secrets-management process or technology and provide supporting evidence. Independent assurance or testing should also be requested where available.

Continued reliance at the current access level should be conditional on addressing the evidence gap.

---

## 3. Guardline Managed Security Services

**Tier:** Tier 2  
**Service:** 24/7 SOC monitoring  
**Owner:** CISO  

### Observed

An ISO 27001 certificate is on file, but the copy available to ApexBridge expired approximately 14 months ago.

### Why It Matters

An expired certificate cannot reliably demonstrate the vendor's current certification status.

The underlying security controls may still be effective, but ApexBridge cannot treat an expired document as current assurance without additional confirmation.

### Evidence Supporting the Observation

- ISO 27001 certificate held in the vendor evidence file
- Certificate expiration date

### Remaining Uncertainty

It is unclear whether:

- Guardline has renewed its certification and ApexBridge simply has an outdated copy, or
- The certification has actually lapsed.

### Risk Implication

Guardline's security posture cannot currently be treated as verified through the certificate.

Importantly, this does not mean the vendor is necessarily insecure. The issue is that the available evidence is no longer current.

### Recommended Action

**Request Additional Evidence**

Request a current ISO 27001 certificate or written confirmation of renewal status.

This should be treated as a straightforward evidence-refresh action rather than an immediate escalation unless the vendor cannot provide reasonable confirmation.

---

## 4. Meridian Pay

**Tier:** Tier 2 — Borderline Tier 1  
**Service:** Payment gateway  
**Owner:** Finance Director  

### Observed

Meridian provided a self-completed PCI Self-Assessment Questionnaire rather than independent PCI validation. The assessment also identified reliance on an underlying payment processor that has not yet been fully disclosed to ApexBridge.

### Why It Matters

Meridian is revenue-critical and operates in a payment-related environment.

Tokenization reduces ApexBridge's direct exposure because ApexBridge does not handle raw card data. However, Meridian's reliance on another processor introduces fourth-party dependency that can affect ApexBridge's overall risk exposure.

### Evidence Supporting the Observation

- PCI Self-Assessment Questionnaire
- Tokenization architecture description
- Confirmation that ApexBridge does not handle raw card numbers

### Remaining Uncertainty

ApexBridge does not currently have sufficient visibility into:

- The underlying payment processor
- Its relevant security assurance
- The scope of its responsibilities
- Whether independent PCI validation is available

### Risk Implication

Tokenization is a genuine mitigating factor and reduces ApexBridge's direct payment-data exposure.

However, the fourth-party dependency and reliance on self-attestation mean residual risk is not fully resolved.

### Recommended Action

**Proceed With Conditions**

Continue the relationship given the existing tokenization mitigation, while requiring:

- Disclosure of the relevant underlying payment processor
- Review of available fourth-party assurance
- Independent PCI validation, if available
- Reassessment at the next renewal or following a material change

The vendor should remain subject to enhanced monitoring until the evidence gap is resolved.

---

## 5. Brightloop Marketing Automation

**Tier:** Tier 3  
**Service:** Email marketing automation  
**Owner:** Marketing Director  

### Observed

Brightloop has almost no security documentation on file beyond publicly available SaaS terms of service.

### Why It Matters

A lack of security documentation can initially appear concerning. However, risk must be evaluated against actual exposure.

Brightloop has no system access, handles only prospect/customer contact information, has low business criticality, and can be replaced relatively easily.

### Evidence Supporting the Observation

- Publicly available SaaS terms of service
- Existing vendor inventory information
- Confirmed lack of system access
- Low business dependency

### Remaining Uncertainty

There is limited uncertainty about the vendor's overall risk profile.

The primary unknown is the detail of Brightloop's security and data-handling practices, rather than whether the vendor presents significant system or operational exposure.

### Risk Implication

Residual risk remains low and is broadly consistent with the vendor's inherent risk.

The documentation gap does not justify treating Brightloop like a Tier 1 or Tier 2 vendor.

### Recommended Action

**Proceed**

A light-touch confirmation of data-handling practices is sufficient.

A full security questionnaire or extensive evidence request would not be proportionate to the vendor's actual exposure.

---

## 6. Ferrow Analytics

**Tier:** Not Yet Tiered  
**Service:** Data analytics contractor  
**Owner:** Director of Product Analytics  

### Observed

An owner has now been identified, and Ferrow has confirmed access to a raw, unclassified customer dataset.

However, the assessment has not formally begun and the scope of access remains unclear.

### Why It Matters

This changes the risk picture significantly.

Ferrow is no longer simply an unidentified or incomplete vendor record. There is now confirmed access to real customer data, while critical assessment information remains unresolved.

This creates a more urgent situation than the original "Not Yet Tiered" status suggested.

### Evidence Supporting the Observation

- Owner confirmation
- Confirmation of access to a raw customer dataset
- Partial description of the analytics work performed

### Remaining Uncertainty

Significant information remains unknown, including:

- Formal data classification
- Exact access scope
- Access architecture
- Security controls
- Subcontractor involvement
- Business criticality
- Data retention and handling practices

### Risk Implication

The vendor's residual risk cannot yet be estimated with confidence.

However, confirmed access to raw customer data justifies treating Ferrow as an **elevated assessment priority**.

The available facts are sufficient to justify urgent assessment, but not sufficient to assign a final Tier 1 or Tier 2 classification.

### Recommended Action

**Escalate for Prioritized Full Assessment**

Move Ferrow to the front of the next assessment cycle.

The assessment should establish data classification, access scope, security controls, subcontractor use, and business criticality before a final tier is assigned.

Ferrow should not remain indefinitely in a "Not Yet Tiered" holding state simply because the information is incomplete.

---

## Overall Assessment Takeaway

The six vendors demonstrate why third-party risk assessment cannot be reduced to checking whether documents exist.

The important questions are:

1. **Is the evidence current?**
2. **Does the evidence actually cover the relevant control?**
3. **Is the evidence independently reliable?**
4. **Does the evidence match the vendor's actual risk exposure?**
5. **What remains unknown?**
6. **What action is proportionate to the residual risk?**

The assessment therefore distinguishes between several different conditions:

- **NorthPeak:** Evidence exists, but the **scope does not clearly cover the relevant risk**.
- **Corestack:** High inherent risk with **insufficient independent evidence**.
- **Guardline:** Evidence exists, but it is **expired**.
- **Meridian:** Risk is partly mitigated, but **fourth-party dependency and self-attestation remain**.
- **Brightloop:** Evidence is weak, but **low inherent risk makes a light-touch approach appropriate**.
- **Ferrow:** Information is incomplete, but **confirmed customer-data access makes the uncertainty urgent**.

### Key Principle

> **Evidence quality and risk are related, but they are not the same thing.**

A vendor with limited documentation is not automatically high risk, and a vendor with impressive documentation is not automatically low risk. The assessment decision depends on whether the available evidence actually supports confidence in the controls that matter.