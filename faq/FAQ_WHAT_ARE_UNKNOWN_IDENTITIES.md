---
title: "What are unknown identities?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0049
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0095
knowledge_relationships:
  depends_on:
    - KID-CON-0095
  explains:
    - KID-CON-0095
website_slug: faq-what-are-unknown-identities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Unknown identities appear in logs or directories but lack enough context for confident prioritization—uncertainty about role, ownership, or privilege, not simply an unmapped username."
---

# What are unknown identities?

## Short answer

**Unknown identities** are users or service accounts that **appear in activity or directory sources** but lack **enough context** for confident security decisions—uncertainty about role, ownership, or privilege, not simply an unmapped username.

## Explanation

Authentication logs, cloud audit trails, and federation events may surface principals before anyone assigns meaning to them. Until context is enriched, analysts should treat these as **decision gaps**: activity may be real, but priority and blast radius are unreliable. Resolving unknown identities means improving **context**, not only closing directory tickets.

Guide: [Unknown Identities](../knowledge/UNKNOWN_IDENTITIES.md) (`KID-CON-0095`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-009) |
