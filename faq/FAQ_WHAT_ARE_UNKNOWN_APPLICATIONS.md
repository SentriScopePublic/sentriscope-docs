---
title: "What are unknown applications?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0054
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0105
knowledge_relationships:
  depends_on:
    - KID-CON-0105
  explains:
    - KID-CON-0105
website_slug: faq-what-are-unknown-applications
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Unknown applications exist in activity or integration sources but lack enough context for confident security decisions—uncertainty about business function and ownership, not simply a missing catalog entry."
---

# What are unknown applications?

## Short answer

**Unknown applications** are software capabilities that **exist in activity or integration sources** but lack **enough context** for confident security decisions—uncertainty about **business function**, **ownership**, or **data scope**, not simply a missing service catalog entry.

## Explanation

Logs, identity federation, and SaaS admin consoles may surface access to a capability before anyone assigns business meaning to it. Until context is enriched, analysts should treat these as **decision gaps**: findings may be real, but priority, blast radius, and stakeholder narrative are unreliable. Resolving unknown applications means improving **context**, not only closing inventory tickets.

Guide: [Unknown Applications](../knowledge/UNKNOWN_APPLICATIONS.md) (`KID-CON-0105`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-010) |
