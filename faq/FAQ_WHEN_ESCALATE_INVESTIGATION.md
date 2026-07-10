---
title: "When should a security investigation be escalated?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0015
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0023
  - KID-CON-0005
  - KID-CON-0024
knowledge_relationships:
  depends_on:
    - KID-CON-0023
  explains:
    - KID-CON-0023
  authority_reference:
    - KID-INV-0001
website_slug: faq-when-escalate-investigation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Escalate when decision stakes exceed current confidence, active harm is likely, scope exceeds team authority, or regulatory and legal thresholds are met—document rationale either way."
---

# When should a security investigation be escalated?

## Short answer

Escalate when **stakes exceed confidence**, **active harm is likely**, **scope exceeds team authority**, or **regulatory/legal thresholds** apply—even if evidence is incomplete.

## Explanation

Decision framework: [Investigation Decisions](../knowledge/INVESTIGATION_DECISIONS.md) (`KID-CON-0023`).

| Signal | Typical escalation |
|--------|-------------------|
| Confirmed active exploitation | IR / containment |
| Critical asset, low confidence | Tier 2 / senior analyst |
| Legal or regulatory exposure | Legal, compliance, executive |
| Cross-organizational scope | Central IR or CSIRT |

**High stakes + low confidence** often warrants escalation **and** protective action while investigation continues.

## Related

- [Security Investigation vs Incident Response](../knowledge/SECURITY_INVESTIGATION_VS_INCIDENT_RESPONSE.md) — `KID-CON-0005`
- [Investigation Prioritization](../knowledge/INVESTIGATION_PRIORITIZATION.md) — `KID-CON-0024`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ — SER-002 |
