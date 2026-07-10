---
title: "What is correlation?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0061
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0120
knowledge_relationships:
  depends_on:
    - KID-CON-0120
  explains:
    - KID-CON-0120
    - KID-GLS-0013
website_slug: faq-what-is-correlation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Correlation links related security observations into coherent stories so analysts act on meaning—not isolated alerts or duplicate tickets for the same underlying issue."
---

# What is correlation?

## Short answer

**Correlation** is the process of linking **related security observations**—findings, assets, identities, exposures, and intelligence—into a coherent story that informs a decision. It answers: *Do these items belong together?* *Does this change what we should do?*

## Explanation

Practitioners often confuse correlation with alert deduplication or dashboard grouping. Correlation is **decision-oriented**: it connects observations because they **mutually inform** prioritization, investigation scope, or risk communication—not merely because they share a timestamp or severity.

Effective correlation is entity-aware, continuous as new data arrives, and explicit when linkage is uncertain.

Term authority: [Correlation](../glossary/CORRELATION.md) (`KID-GLS-0013`).

Guide: [Understanding Correlation](../knowledge/UNDERSTANDING_CORRELATION.md) (`KID-CON-0120`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-012) |
