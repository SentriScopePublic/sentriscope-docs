---
title: "Understanding Operational Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0060
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0006
    - KID-CON-0058
    - KID-CON-0030
  explains:
    - KID-GLS-0006
  related_to:
    - KID-CON-0061
    - KID-CON-0062
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-006
  editorial_season: SEA-004
  pillar_page: PIL-OP-INTEL
  learning_path: LP-006
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0058
    - KID-GLS-0006
  recommended_next:
    - KID-CON-0061
website_slug: understanding-operational-intelligence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational intelligence transforms internal operational knowledge—assets, telemetry, controls, queue state—into explainable prioritization for better security decisions, not SIEM operations or tool configuration."
knowledge_tags: [operational-intelligence, education, decision-support]
---

# Understanding Operational Intelligence

## What practitioners need to know

Practitioners ask: *What is operational intelligence?* *Is it the same as a SIEM?*

**Operational intelligence** transforms **internal operational knowledge** into **better security decisions**—where to focus attention now, with explainable reasons tied to your organization's state.

Term authority: [Operational Intelligence](../glossary/OPERATIONAL_INTELLIGENCE.md) (`KID-GLS-0006`).

## TI vs OI boundary

| Dimension | Threat Intelligence (SER-005) | Operational Intelligence (SER-006) |
|-----------|------------------------------|--------------------------------------|
| **Environment** | External | Internal |
| **Focus** | Threat actors, campaigns | Organization state |
| **Inputs** | Reports, feeds, sharing | Assets, identities, telemetry, controls |
| **Context** | Global threat landscape | Local operational context |
| **Consumers** | Intel analysts, hunters | Operational decision-makers |

## What operational intelligence is

| OI is | OI is not |
|-------|-----------|
| Decision-support from internal state | SIEM query tutorials |
| Explainable prioritization | Autonomous SOC |
| Bridge from data to decisions | Raw log storage |
| Context for investigations | Compliance snapshot only |

## Connection to Volume 1 and SER-005

```text
Volume 1: Evidence → Investigation → Risk → Attack Paths
SER-005: External knowledge → decisions
SER-006: Internal knowledge → decisions
```

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Confusing OI with tool dashboards | Activity without decisions |
| Ignoring explainability | Priority distrust |
| OI without asset context | Wrong focus |
| Replacing investigation with queues | Shallow closures |

## Practical implications

1. **Ask what decision OI changes** before acting on rank.  
2. **Link rank to reason codes** stakeholders can audit.  
3. **Combine with TI** when external context applies (`KID-CON-0053`).  

## Limitations

OI quality depends on data normalization, inventory accuracy, and model scope—incomplete internals produce incomplete prioritization.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0031 | [What is operational intelligence?](../faq/FAQ_WHAT_IS_OPERATIONAL_INTELLIGENCE.md) |
| KID-CON-0068 | [Operational Intelligence as Decision Support](./OPERATIONAL_INTELLIGENCE_AS_DECISION_SUPPORT.md) |

## Authority references

- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-006 article |
