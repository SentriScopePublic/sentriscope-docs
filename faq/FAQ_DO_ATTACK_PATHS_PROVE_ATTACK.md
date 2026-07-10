---
title: "Do attack paths prove an active attack?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0022
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0040
  - KID-CON-0044
  - KID-CON-0048
knowledge_relationships:
  depends_on:
    - KID-GLS-0011
  explains:
    - KID-CON-0040
website_slug: faq-do-attack-paths-prove-attack
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "No—attack paths are structural hypotheses about plausible compromise sequences; active attack requires investigation evidence."
---

# Do attack paths prove an active attack?

## Short answer

**No.** Attack paths are **structural hypotheses**—plausible sequences showing how compromise *could* propagate. They do **not** prove an attack is underway.

## Explanation

Use paths to **prioritize** and **scope investigation**. Validate each hop with logs, telemetry, and forensic evidence before concluding active compromise.

Guide: [Attack Paths in Investigation](../knowledge/ATTACK_PATHS_IN_INVESTIGATION.md) (`KID-CON-0048`).

## Common mistake

Escalating or declaring incident status based on a graph edge alone.

## Authority references

- [Attack Path](../glossary/ATTACK_PATH.md) — `KID-GLS-0011`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-004) |
