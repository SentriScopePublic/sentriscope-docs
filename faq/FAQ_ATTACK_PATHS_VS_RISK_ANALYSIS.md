---
title: "Do attack paths replace risk analysis?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0025
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0044
  - KID-CON-0049
  - KID-CON-0031
knowledge_relationships:
  depends_on:
    - KID-CON-0049
    - KID-CON-0031
  explains:
    - KID-CON-0049
  authority_reference:
    - KID-GLS-0023
website_slug: faq-attack-paths-vs-risk-analysis
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "No—attack paths provide structural context that informs risk prioritization; they do not replace risk analysis, judgment, or acceptance decisions."
---

# Do attack paths replace risk analysis?

## Short answer

**No.** Attack paths provide **structural context**—reachability and chains—that **feeds** risk prioritization. Analyst judgment, business context, and acceptance decisions remain essential.

## Explanation

Think: **risk analysis decides priority; paths explain structural why**. When they conflict, document the resolution explicitly.

Guides: [Attack Paths as Decision Support](../knowledge/ATTACK_PATHS_AS_DECISION_SUPPORT.md) (`KID-CON-0049`), [Risk Prioritization in Practice](../knowledge/RISK_PRIORITIZATION_IN_PRACTICE.md) (`KID-CON-0031`).

## Common mistake

Letting the graph rank queue automatically without risk context layers.

## Authority references

- [Decision Support](../glossary/DECISION_SUPPORT.md) — `KID-GLS-0023`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-004) |
