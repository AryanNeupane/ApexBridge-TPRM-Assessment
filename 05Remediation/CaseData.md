# ApexBridge Technologies — Findings Summary

## F-002 — Corestack: Privileged Deployment Access Without Secrets Management

**Severity:** High

**Situation:**  
Corestack holds privileged deployment access to ApexBridge production repositories with no defined or evidenced credential management.

Corestack has responded that the change cannot ship until next quarter. The VP Engineering says ApexBridge cannot wait because Corestack sits in the deployment path for every release.

**Complicating Factor:**  
This is simultaneously the highest-risk finding and the one attached to the most strategically embedded vendor.

"Reject the vendor" is not a serious option, and neither is waiting quietly.

---

## F-006 — Corestack: Penetration Test Currency

**Severity:** Medium

**Situation:**  
The penetration test on file is 26 months old and predates a major platform release.

This was split out from F-002 during treatment planning because it requires a different action and a different timeline.

Other Corestack controls described in their access control policy appear reasonable in design.

---

## F-003 — Meridian Pay: Unassessed Payment Subprocessor

**Severity:** Medium

**Situation:**  
The primary payment processor underneath Meridian Pay is now named but remains unassessed.

Meridian is unlikely to provide assurance evidence on a party it does not control. ApexBridge's direct card-data exposure is bounded by tokenization.

The Finance Director has asked whether 90 days is really necessary for a Medium finding.

---

## F-005 — Ferrow Analytics: Incomplete Assessment

**Severity:** Medium

**Situation:**  
The questionnaire is 60% complete, with retention, subcontractor use, and access management left blank.

Ferrow has also confirmed access to a raw customer dataset.

The tier assignment has been pending since Day 2 and cannot be finalized until these sections are answered.

---

## F-001 — NorthPeak: SOC 2 Scope Limitation

**Severity:** Medium

**Situation:**  
NorthPeak has declined to expand their SOC 2 scope — normal for a provider at their scale and not a signal of evasion.

They have instead offered an ISO 27001 certificate whose scope statement covers the hosting platform, including logical access management, plus their CUEC documentation.

Exposure is bounded because the CUECs confirm that ApexBridge controls its own tenant-level access.

---

## F-004 — Guardline: Evidence Currency Monitoring Gap

**Severity:** Low

**Situation:**  
ApexBridge held an expired certificate copy with nothing prompting a refresh.

Guardline renewed on time.

This is an internal process gap with minimal security impact, but it is systemic because the same blind spot applies to every vendor's evidence.

---

## OBS-01 — Brightloop: Closed Observation

**Status:** Closed — No Treatment Required

**Situation:**  
OBS-01 was closed as an observation on Day 4 and requires no treatment.

It remains in the register as a closed item rather than disappearing.

A closed observation provides evidence that proportionality was applied and that not every identified issue was unnecessarily escalated into a formal finding.