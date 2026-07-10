---
title: "What Makes Security Evidence Trustworthy"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0002
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-CON-0001
  explains:
    - KID-GLS-0001
  related_to:
    - KID-CON-0003
  authority_reference:
    - KID-INV-0001
website_slug: what-makes-security-evidence-trustworthy
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "Trustworthy security evidence has provenance, corroboration, freshness appropriate to the decision, and explicit confidence—not merely a high severity label or single-source claims."
knowledge_tags: [evidence, education]
---

# What Makes Security Evidence Trustworthy

## What practitioners need to know

Trustworthy **evidence** is information you can defend under scrutiny. Practitioners ask: *Can I rely on this for a production decision?*

Evaluate evidence on dimensions—not a single severity field.

## Trust dimensions

| Dimension | Question |
|-----------|----------|
| **Provenance** | Where did this come from? Can I trace it? |
| **Freshness** | Is it current enough for this decision? |
| **Corroboration** | Do independent sources agree? |
| **Specificity** | Does it link to entities (asset, identity) not abstract labels? |
| **Contradiction handling** | What disconfirms this? Was it considered? |
| **Source credibility** | Is the originating system authoritative for this claim? |

## Common mistakes

- **Single-source conviction** — one EDR alert without asset validation  
- **Stale evidence** — CMDB record months old during active incident  
- **Anonymous exports** — CSV with no source_system metadata  
- **Confusing confidence with severity** — critical label ≠ validated exploit  

## Practical implications

Build investigation habits that **grade evidence quality** before escalation. Low-trust evidence may still warrant exploration—it should not silently drive emergency change without corroboration.

Term authority: [Evidence](../glossary/EVIDENCE.md) (`KID-GLS-0001`). Investigation patterns: `KID-CON-0001`.

## Related knowledge

- `KID-CON-0001` — Evidence-Based Investigation  
- `KID-FAQ-0001` — Alert vs evidence  

## Authority references

- `KID-INV-0001` — evidence governance in investigation workflows  

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial encyclopedia article |
