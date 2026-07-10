---
title: "When should I ignore attack paths?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0024
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0047
  - KID-CON-0043
knowledge_relationships:
  depends_on:
    - KID-CON-0047
  explains:
    - KID-CON-0047
website_slug: faq-when-ignore-attack-paths
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Ignore or override path guidance when graph data is too stale, confidence is low, active compromise uses non-structural vectors, or policy mandates action outside path rank."
---

# When should I ignore attack paths?

## Short answer

Override or defer path guidance when **graph confidence is low**, **inventory is incomplete**, **active compromise uses non-path vectors**, or **mandated actions** (compliance, confirmed incident) take precedence.

## Explanation

Paths optimize **structural** decisions. They do not replace threat intelligence, behavioral detection, or investigation evidence.

Guide: [When Attack Paths Are Not Enough](../knowledge/WHEN_ATTACK_PATHS_ARE_NOT_ENOUGH.md) (`KID-CON-0047`).

## Common mistake

Treating path absence as proof of safety—or path presence as proof of breach.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-004) |
