---
title: "How do attack paths help prioritization?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0023
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0042
  - KID-CON-0045
knowledge_relationships:
  depends_on:
    - KID-CON-0042
  explains:
    - KID-CON-0042
  authority_reference:
    - KID-OIN-0001
website_slug: faq-how-attack-paths-help-prioritization
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack paths reveal reachability to high-value targets, choke points, and chained exposure that flat severity lists miss—providing context for risk prioritization."
---

# How do attack paths help prioritization?

## Short answer

Paths show **what could be reached** if a step fails—surfacing **choke points**, **crown-jewel reachability**, and **low-severity chains** that flat CVE sorts miss.

## Explanation

Paths **inform** rank; they do not replace risk judgment. Combine path context with exposure, asset tier, controls, and threat activity.

Guide: [Why Attack Paths Change Priorities](../knowledge/WHY_ATTACK_PATHS_CHANGE_PRIORITIES.md) (`KID-CON-0042`).

## Common mistake

Auto-promoting every node on any path without context or documented rationale.

## Authority references

- `KID-OIN-0001` — operational intelligence context

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-004) |
