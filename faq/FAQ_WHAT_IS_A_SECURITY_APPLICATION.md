---
title: "What is a security application?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0051
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0100
knowledge_relationships:
  depends_on:
    - KID-CON-0100
  explains:
    - KID-CON-0100
website_slug: faq-what-is-a-security-application
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security application is the software capability that delivers a business function and anchors findings, access, and investigations—not a catalog row or deployment name alone."
---

# What is a security application?

## Short answer

A **security application** is a **software capability** that delivers a **business function** and can be **affected**, **abused**, or **reached** in compromise. It is a **decision lens**, not just a service catalog entry or repository name.

## Explanation

Applications matter because security work attaches to **what business function could fail**: the same OAuth misconfiguration on an internal HR sandbox is not the same decision as on a customer payment portal. Context—business purpose, data class, users, and relationships—changes what analysts prioritize and how they explain blast radius.

Guide: [Understanding Security Applications](../knowledge/UNDERSTANDING_SECURITY_APPLICATIONS.md) (`KID-CON-0100`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-010) |
