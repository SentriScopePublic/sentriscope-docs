---
title: "What is operational intelligence?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0003
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0060
  - KID-GLS-0006
knowledge_relationships:
  depends_on:
    - KID-GLS-0006
  explains:
    - KID-GLS-0006
  authority_reference:
    - KID-OIN-0001
website_slug: faq-what-is-operational-intelligence
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "Operational intelligence aggregates normalized security data into explainable prioritization so teams know where to focus attention now—not a SIEM replacement or autonomous SOC."
---

# What is operational intelligence?

## Short answer

**Operational intelligence** is the practice of turning normalized security data into **explainable prioritization**—helping teams decide **where to focus attention now**, with reasons tied to risk, coverage, and threat context.

## Explanation

Security teams drown in disconnected queues. Operational intelligence sits above raw tool output: it correlates signals into ranked **attention** with explainable reason codes, then feeds investigation and remediation workflows.

It differs from:

- **Threat intelligence** — external CTI focus (`KID-GLS-0005`, `KID-TIN-0001`)
- **SIEM** — event detection and log-centric pipelines (`KID-PLT-0002`)
- **Compliance reporting** — periodic posture snapshots

## Common mistake

Expecting operational intelligence to **execute** responses autonomously. It prioritizes and explains; humans (and governed workflows) decide and act.

## Authority references

- [Operational Intelligence](./../glossary/OPERATIONAL_INTELLIGENCE.md) — `KID-GLS-0006`
- [Operational Intelligence capability](./../intelligence/OPERATIONAL_INTELLIGENCE.md) — `KID-OIN-0001`

## Related

- [From Alerts to Decisions](./../knowledge/FROM_ALERTS_TO_DECISIONS.md) — `KID-CON-0008`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ |
