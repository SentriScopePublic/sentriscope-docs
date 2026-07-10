---
title: "What is the difference between identity and account?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0047
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0091
knowledge_relationships:
  depends_on:
    - KID-CON-0091
  explains:
    - KID-CON-0091
website_slug: faq-identity-vs-account-difference
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "An account is often a technical credential or login record; a security identity is the decision lens that combines accounts, roles, and context so analysts can judge access and blast radius."
---

# What is the difference between identity and account?

## Short answer

An **account** is often a **technical credential or login record** in a system. A **security identity** is the **decision lens** that combines accounts, roles, ownership, and context so analysts can judge **access and blast radius**—not merely whether a username exists.

## Explanation

Directories and cloud platforms create many account objects—local users, federated logins, service principals. Security decisions require knowing **who or what the account represents**, **what it can reach**, and **whether activity is expected**. Treating every account row as a complete identity leads to flat prioritization and missed pivot points in investigations.

Guide: [Identity vs Account](../knowledge/IDENTITY_VS_ACCOUNT.md) (`KID-CON-0091`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-009) |
