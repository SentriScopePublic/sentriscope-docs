---
title: "What are unknown assets?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0043
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0084
knowledge_relationships:
  depends_on:
    - KID-CON-0084
  explains:
    - KID-CON-0084
website_slug: faq-what-are-unknown-assets
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Unknown assets exist in the environment but lack enough context for confident prioritization—uncertainty about role and impact, not simply a missing inventory record."
---

# What are unknown assets?

## Short answer

**Unknown assets** are entities that **exist in your environment** but lack **enough context** for confident security decisions—uncertainty about business role, ownership, or impact, not simply a missing CMDB entry.

## Explanation

Discovery tools may detect a host or cloud resource before anyone assigns meaning to it. Until context is enriched, analysts should treat these as **decision gaps**: findings may be real, but priority and blast radius are unreliable. Resolving unknown assets means improving **context**, not only closing inventory tickets.

Guide: [Unknown Assets](../knowledge/UNKNOWN_ASSETS.md) (`KID-CON-0084`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-008) |
