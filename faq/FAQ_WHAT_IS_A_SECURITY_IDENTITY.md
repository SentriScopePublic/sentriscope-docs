---
title: "What is a security identity?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0046
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0090
knowledge_relationships:
  depends_on:
    - KID-CON-0090
  explains:
    - KID-CON-0090
website_slug: faq-what-is-a-security-identity
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security identity is a user or service account that anchors access, activity, and investigations—enriched with context about privilege and relationships that changes how findings are interpreted."
---

# What is a security identity?

## Short answer

A **security identity** is a **user or service account** in your environment—human users, service principals, machine accounts, and similar—that **anchors access, activity, and investigations**. It is a **decision lens**, not just a directory record.

## Explanation

Identities matter because security work attaches to **who or what acted**: the same alert on a contractor account is not the same decision as the same alert on a privileged administrator. Context—[identity privilege](../glossary/IDENTITY_PRIVILEGE.md) (`KID-GLS-0031`), access relationships, and environment—changes what analysts prioritize and how they explain blast radius.

Guide: [Understanding Security Identities](../knowledge/UNDERSTANDING_SECURITY_IDENTITIES.md) (`KID-CON-0090`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-009) |
