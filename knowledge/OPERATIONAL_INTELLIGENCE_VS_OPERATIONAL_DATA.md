---
title: "Operational Intelligence vs Operational Data"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0061
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0060
    - KID-GLS-0001
  related_to:
    - KID-CON-0008
    - KID-GLS-0026
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-006
  pillar_page: PIL-OP-INTEL
  learning_path: LP-006
  difficulty: introductory
  audience: [analyst]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0060
  recommended_next:
    - KID-CON-0062
website_slug: operational-intelligence-vs-operational-data
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational data is raw and normalized security telemetry; operational intelligence is the decision-support layer that prioritizes and explains where operational attention should go."
knowledge_tags: [operational-intelligence, education]
---

# Operational Intelligence vs Operational Data

## What practitioners need to know

Practitioners ask: *We have logs and alerts—isn't that already operational intelligence?*

**Operational data** is what your tools produce. **Operational intelligence** is how you **prioritize and explain** operational attention from that data.

## Comparison

| Dimension | Operational data | Operational intelligence |
|-----------|------------------|--------------------------|
| **Unit** | Events, findings, metrics | Ranked attention with reasons |
| **Question** | What happened? | What should we focus on now? |
| **Output** | Volume | Explainable priority |
| **Consumer** | Pipelines, storage | Decision-makers |
| **Value** | Necessary input | Decision support |

See [From Alerts to Decisions](./FROM_ALERTS_TO_DECISIONS.md) (`KID-CON-0008`) for the maturity path.

## Operational signals

[Operational signals](../glossary/OPERATIONAL_SIGNAL.md) (`KID-GLS-0026`) are normalized inputs—alerts, findings, state changes—that **feed** OI; they are not OI by themselves.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Data lake = intelligence | Analysis paralysis |
| More dashboards = OI | Noise |
| Skipping normalization | Duplicate priority |
| No reason codes | Un auditable rank |

## Practical implications

Invest in **explainable prioritization** over raw collection when queues already overflow.

## Limitations

Without trustworthy [evidence](./WHAT_IS_SECURITY_EVIDENCE.md) (`KID-CON-0010`) discipline, OI ranks unvalidated signals.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0032 | [Is operational intelligence the same as SIEM data?](../faq/FAQ_OI_VS_SIEM_DATA.md) |

## Authority references

- `KID-OIN-0001` — operational intelligence capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-006 article |
