
# raw third-party information


| Vendor | Key Drivers | Tier | What's Missing / Assumed |
|---|---|---|---|
| **NorthPeak Cloud Infrastructure** | Hosts all production; failure stops the core product; holds customer + employee data by extension | **Tier 1** | No documented DR/continuity evidence on file — flagged for Day 3 due diligence |
| **Solvane HR & Payroll** | Sensitive employee PII and banking data; payroll is operationally critical | **Tier 1** | Data classification should be formally tagged, not just inferred |
| **Corestack DevOps Tooling** | Privileged deployment access to production repositories; a compromised pipeline is a severe exposure | **Tier 1** | Existing "Low" tag is stale and should be formally corrected in the inventory, not just overridden ad hoc |
| **Guardline Managed Security Services** | High criticality; loss of service reduces threat visibility; moderate-to-high access to security tooling | **Tier 2** | Consider Tier 1 if production visibility proves broader than currently understood — confirm during Day 3 due diligence |
| **Meridian Pay** | Revenue-critical; touches payment data even if tokenized; regulatory relevance through PCI | **Tier 2 (borderline Tier 1)** | PCI attestation status is unconfirmed — this could reasonably move it to Tier 1; flagged for validation |
| **HelpDeskly** | Customer contact data and support content; moderate operational relevance | **Tier 2** | None material — vendor risk profile is reasonably well understood |
| **PulseSurvey** | Employee PII; survey responses may be sensitive; low criticality, but potential SSO integration would raise access risk | **Tier 2 (pending)** | SSO/directory integration status is unresolved and material to the final tier; must be confirmed before finalizing |
| **Brightloop Marketing Automation** | Prospect/customer contact information only; no system access; low criticality | **Tier 3** | None material |
| **Vantix Legal Services** | Occasional access to sensitive contract drafts; low frequency; no system access; easily replaced | **Tier 3** | None material |
| **Lumen Translate** | Low data sensitivity; no system access; low criticality | **Tier 3** | Contract status must be resolved; no signed agreement located. This is a contracting gap independent of the tier |
| **CrestOffice Supplies** | No data; no access; negligible dependency | **Tier 4** | None |
| **Ferrow Analytics** | Unknown data classification; unknown access scope; unclear whether it represents one vendor or two | **Not Yet Tiered** | Cannot be responsibly tiered until: (1) an owner is assigned, (2) data classification is confirmed, and (3) the duplicate-name question is resolved with Procurement/AP records. Provisionally treated as requiring elevated attention until clarified |