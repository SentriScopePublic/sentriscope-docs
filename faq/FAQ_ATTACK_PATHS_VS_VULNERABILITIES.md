---
title: "Are attack paths the same as vulnerabilities?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0021
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0041
  - KID-CON-0044
knowledge_relationships:
  depends_on:
    - KID-CON-0041
  explains:
    - KID-CON-0041
  authority_reference:
    - KID-GLS-0011
website_slug: faq-attack-paths-vs-vulnerabilities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "No—vulnerabilities describe isolated weaknesses; attack paths show how weaknesses could chain in your environment. Both matter for prioritization."
---

# Are attack paths the same as vulnerabilities?

## Short answer

**No.** A **vulnerability** (e.g., CVE) describes an **isolated weakness**. An **attack path** shows how weaknesses could **chain together** in your environment to reach valuable targets.

## Explanation

Use vulnerabilities for patch hygiene and advisory tracking. Use attack paths for **reachability**, **lateral movement context**, and **choke-point** remediation. Best programs link CVEs to nodes on prioritized paths.

Guide: [Attack Paths vs Individual Vulnerabilities](../knowledge/ATTACK_PATHS_VS_INDIVIDUAL_VULNERABILITIES.md) (`KID-CON-0041`).

## Common mistake

Replacing CVE workflows with path views—or ignoring paths because "we already have CVSS."

## Authority references

- [Attack Path](../glossary/ATTACK_PATH.md) — `KID-GLS-0011`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-004) |
