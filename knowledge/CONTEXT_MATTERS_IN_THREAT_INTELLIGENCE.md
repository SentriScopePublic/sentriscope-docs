---
title: "Context Matters in Threat Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0053
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0030
    - KID-CON-0050
    - KID-GLS-0024
  related_to:
    - KID-CON-0052
    - KID-CON-0057
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0050
    - KID-CON-0030
  recommended_next:
    - KID-CON-0055
website_slug: context-matters-in-threat-intelligence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Threat intelligence requires the same contextual layers as risk analysis—asset exposure, intelligence confidence, relevance, and evidence—or it misleads prioritization."
knowledge_tags: [threat-intelligence, context, education]
---

# Context Matters in Threat Intelligence

## What practitioners need to know

An IoC on a list is not an action in **your** environment until **context** validates relevance.

Practitioners ask: *The feed flagged this hash—should we panic?*

Apply [risk context](./RISK_CONTEXT.md) (`KID-CON-0030`) plus intelligence-specific layers.

## Context checks for TI

| Layer | Intelligence question |
|-------|----------------------|
| **Relevance** | Does this threat target our sector, stack, or geography? |
| **Asset overlap** | Do affected assets or paths exist here? |
| **Exposure** | Are matching systems reachable today? |
| **Confidence** | Source tier, freshness, corroboration (`KID-GLS-0024`) |
| **Evidence** | Internal detection or investigation confirmation? |
| **Timeliness** | Is exploitation still active? |

## Common context failures

| Failure | Effect |
|---------|--------|
| Stale IoC blocklists | False positives |
| High-confidence hype, low relevance | Wasted cycles |
| Missing asset inventory | Irrelevant TI noise |
| TI without path context | Wrong remediation target |

## Practical implications

1. **Contextualize before escalating** TI output.  
2. **Flag low-confidence assessments** explicitly.  
3. **Refresh** when risk context triggers re-rank (`KID-CON-0036`).  
4. **Use investigation** when TI and evidence conflict (`KID-CON-0056`).  

## Limitations

Full contextual validation on every indicator is expensive. Tier depth by **asset tier and intelligence confidence**.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0024 | [Intelligence Confidence](../glossary/INTELLIGENCE_CONFIDENCE.md) |
| KID-CON-0057 | [When Threat Intelligence Is Not Enough](./WHEN_THREAT_INTELLIGENCE_IS_NOT_ENOUGH.md) |

## Authority references

- `KID-ARC-0001` — entity and asset model

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
