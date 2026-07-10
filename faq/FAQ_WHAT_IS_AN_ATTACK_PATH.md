---
title: "What is an attack path?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0002
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0040
  - KID-GLS-0011
knowledge_relationships:
  depends_on:
    - KID-GLS-0011
  explains:
    - KID-GLS-0011
  authority_reference:
    - KID-AGR-0001
website_slug: faq-what-is-an-attack-path
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "An attack path is a plausible multi-step sequence showing how compromise could move through assets and identities—it supports prioritization and investigation but does not prove an attack occurred."
---

# What is an attack path?

## Short answer

An **attack path** is a plausible **multi-step sequence** showing how compromise could move through **assets**, **identities**, and **exposures** in your environment. It helps answer structural impact questions; it does **not** prove an attack is underway.

## Explanation

Practitioners use attack paths to prioritize remediation and investigation: *If this entry point is exploited, what could be reached?* Paths combine relationships—network reachability, identity access, vulnerabilities—not isolated CVSS scores.

Paths are **snapshot-bound** and **model-bound**: they reflect integrated data at a point in time, with stated confidence. Analysts interpret relevance during [investigation](./../glossary/INVESTIGATION.md) (`KID-GLS-0002`).

## Common mistake

Confusing a graph visualization with actionable priority. The value is ranked, explainable paths tied to context—not drawing every possible edge.

## Authority references

- [Attack Path](./../glossary/ATTACK_PATH.md) — `KID-GLS-0011`
- [Attack Graph Overview](./../capabilities/ATTACK_GRAPH_OVERVIEW.md) — `KID-AGR-0001`

## Related

- [Understanding Attack Paths](./../knowledge/UNDERSTANDING_ATTACK_PATHS.md) — `KID-CON-0040`
- [SER-004 Attack Paths](./../knowledge/SERIES_004_ATTACK_PATHS.md)
- [Why Correlation Matters](./../knowledge/WHY_CORRELATION_MATTERS.md) — `KID-CON-0009`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ |
