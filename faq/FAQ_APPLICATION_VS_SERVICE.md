---
title: "What is the difference between application and service?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0052
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0101
knowledge_relationships:
  depends_on:
    - KID-CON-0101
  explains:
    - KID-CON-0101
website_slug: faq-application-vs-service
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security application is the analyst's decision object for business capability at risk; a security service is the exposed technical unit that delivers it—related but not interchangeable when scoping investigations."
---

# What is the difference between application and service?

## Short answer

A **security application** is the **decision object** for **what business capability is at risk**. A **security service** is often the **technical unit**—an API, hosted workload, or endpoint—that **delivers** part of that capability. They are related but **not interchangeable** when scoping investigations and blast radius.

## Explanation

Logs and scanners usually name **services** (`api-payments-v2`, a SaaS tenant, an internal hostname). Stakeholders and regulators ask about **applications** (customer checkout, finance reporting, partner portal). Analysts **map services to applications**—or document when that mapping fails—before containment and escalation narratives are complete.

Guide: [Applications vs Services](../knowledge/APPLICATIONS_VS_SERVICES.md) (`KID-CON-0101`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-010) |
