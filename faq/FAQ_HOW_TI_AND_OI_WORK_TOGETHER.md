---
title: "How do threat and operational intelligence work together?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0037
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0071
  - KID-CON-0070
knowledge_relationships:
  depends_on:
    - KID-CON-0071
  explains:
    - KID-CON-0071
website_slug: faq-how-ti-and-oi-work-together
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "TI and OI work together by correlating external threat relevance with internal operational state to produce reconciled priorities with documented rationale."
---

# How do threat and operational intelligence work together?

## Short answer

**Threat intelligence** supplies **external** context (campaigns, exploitation, TTPs). **Operational intelligence** supplies **internal** context (assets, telemetry, queues, controls). Together they **correlate**—mapping external signals to internal state and **reconciling** rank before decisions reach stakeholders.

## Explanation

Integration is not running two dashboards side by side. It requires **mapping**, **reconciliation rules**, and **documented conflict resolution** when TI and OI disagree.

Guide: [Integrating Threat and Operational Intelligence](../knowledge/INTEGRATING_THREAT_AND_OPERATIONAL_INTELLIGENCE.md) (`KID-CON-0071`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-007) |
