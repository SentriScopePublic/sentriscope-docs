---
title: "When Threat Intelligence Is Not Enough"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0057
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0053
    - KID-CON-0047
  related_to:
    - KID-CON-0054
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0053
  recommended_next:
    - KID-CON-0058
website_slug: when-threat-intelligence-is-not-enough
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Threat intelligence does not replace internal evidence, asset inventory, risk analysis, or detection—know when to supplement or override TI guidance."
knowledge_tags: [threat-intelligence, limitations, education]
---

# When Threat Intelligence Is Not Enough

## What practitioners need to know

Threat intelligence is powerful **external context**—not a complete security program.

Practitioners ask: *When should I ignore or override TI guidance?*

## Gaps TI does not cover

| Gap | What to use instead |
|-----|---------------------|
| **Novel internal misconfiguration** | Risk context, scanning (`SER-003`) |
| **Insider or fraud abuse** | Investigation, non-TI controls |
| **Zero visibility environments** | Inventory remediation first |
| **TI–evidence conflict** | Investigation wins (`KID-CON-0029`) |
| **Compliance mandate** | Policy track parallel to TI |
| **Unmapped intelligence** | Asset mapping before action |
| **Low-confidence rumor** | Corroboration or defer |

Parallel: [When Attack Paths Are Not Enough](./WHEN_ATTACK_PATHS_ARE_NOT_ENOUGH.md) (`KID-CON-0047`).

## Override signals

- Internal evidence disproves TI relevance  
- Intelligence confidence below team threshold  
- Retracted or superseded reporting  
- Business-critical change window unrelated to TI  

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| TI-only program | Blind to internal issues |
| Ignoring TI entirely | Missed exploitation windows |
| Waiting for perfect intel | Paralysis during active campaigns |

## Practical implications

Define **supplement triggers** in runbooks: when TI is insufficient, which capability owns the decision.

## Limitations

SER-006 Operational Intelligence addresses **internal** knowledge gaps TI cannot fill.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0029 | [When should I ignore threat intelligence?](../faq/FAQ_WHEN_IGNORE_THREAT_INTELLIGENCE.md) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
