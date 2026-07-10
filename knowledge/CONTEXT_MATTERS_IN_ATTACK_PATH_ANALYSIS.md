---
title: "Context Matters in Attack Path Analysis"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0043
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0030
    - KID-CON-0040
    - KID-GLS-0003
  related_to:
    - KID-CON-0042
    - KID-CON-0047
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0040
    - KID-CON-0030
  recommended_next:
    - KID-CON-0044
website_slug: context-matters-in-attack-path-analysis
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack path analysis requires the same context layers as risk prioritization—exposure, asset role, identity privilege, controls, and threat activity—or paths mislead decisions."
knowledge_tags: [attack-path, context, education]
---

# Context Matters in Attack Path Analysis

## What practitioners need to know

A path on paper is not a path in **your** environment until **context** validates it.

Practitioners ask: *The tool shows a path—should I trust it?*

Apply [risk context](./RISK_CONTEXT.md) (`KID-CON-0030`) layers to every path step.

## Context checks for paths

| Layer | Path question |
|-------|---------------|
| **Exposure** | Is each hop actually reachable today? |
| **Asset role** | Does the target still matter? |
| **Identity** | Are privileges current? MFA enforced? |
| **Controls** | Does segmentation block this step? |
| **Threat** | Is this chain actively exploited? |
| **Evidence** | Is node state validated or assumed? |

## Common context failures

| Failure | Effect on path |
|---------|----------------|
| Stale CMDB tier | Wrong target importance |
| Missing MFA status | Inflated identity hop |
| Outdated firewall rules | False lateral edge |
| Decommissioned asset | Ghost path |

## Practical implications

1. **Contextualize before escalating** path output.  
2. **Flag low-confidence hops** explicitly.  
3. **Refresh context** on the same triggers as risk re-rank (`KID-CON-0036`).  
4. **Use investigation** when context gaps are high (`KID-CON-0048`).  

## Limitations

Full context on every hop is expensive. Tier validation depth by **path rank and asset tier**.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0003 | [Security Context](../glossary/SECURITY_CONTEXT.md) |
| KID-CON-0047 | [When Attack Paths Are Not Enough](./WHEN_ATTACK_PATHS_ARE_NOT_ENOUGH.md) |

## Authority references

- `KID-ARC-0001` — entity context model

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
