---
title: "Why does identity change investigation scope?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0048
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0097
knowledge_relationships:
  depends_on:
    - KID-CON-0097
  explains:
    - KID-CON-0097
website_slug: faq-why-identity-changes-investigation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Identity changes investigation scope because privilege, access paths, and credential reuse determine what an actor can reach—expanding or narrowing blast radius and follow-up questions."
---

# Why does identity change investigation scope?

## Short answer

**Identity changes investigation scope** because **privilege, access paths, and credential reuse** determine what an actor can reach. The same suspicious event on a low-privilege user and a domain administrator requires **different follow-up**, timeline depth, and stakeholder communication—not the same checklist.

## Explanation

Investigations pivot on **who acted**. Identity context—roles, group membership, recent privilege changes, and cross-system access—defines which assets, applications, and data sets enter scope. Without identity enrichment, teams under-investigate high-blast-radius actors or over-investigate low-impact accounts.

Guide: [Identity in Investigations](../knowledge/IDENTITY_IN_INVESTIGATIONS.md) (`KID-CON-0097`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-009) |
