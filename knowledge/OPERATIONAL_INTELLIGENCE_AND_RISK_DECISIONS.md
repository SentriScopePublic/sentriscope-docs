---
title: "Operational Intelligence and Risk Decisions"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0066
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0031
    - KID-CON-0063
  related_to:
    - KID-CON-0052
    - KID-CON-0042
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-006
  pillar_page: PIL-OP-INTEL
  learning_path: LP-006
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0031
    - KID-CON-0063
  recommended_next:
    - KID-CON-0067
website_slug: operational-intelligence-and-risk-decisions
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational intelligence enriches risk prioritization with live internal state—controls, exposure, queue impact—complementing risk intelligence without replacing judgment."
knowledge_tags: [operational-intelligence, risk, education]
---

# Operational Intelligence and Risk Decisions

## What practitioners need to know

[Risk prioritization](./RISK_PRIORITIZATION_IN_PRACTICE.md) (`KID-CON-0031`) uses context layers. **Operational intelligence** supplies **live internal state** that static risk snapshots miss.

Practitioners ask: *How does OI differ from risk intelligence?*

| Risk intelligence (SER-003) | Operational intelligence (SER-006) |
|----------------------------|-------------------------------------|
| Framework for prioritizing risk | Live operational state feeding rank |
| Context layers (conceptual) | Current queue and control reality |
| Analyst judgment model | Explainable operational rank input |

They **combine**—not compete.

## How OI enriches risk decisions

| Risk question | OI input |
|---------------|----------|
| Is this still exposed? | Current reachability state |
| Are controls effective? | Degraded control signals |
| What fails if we defer? | Operational dependency view |
| Did TI elevate this? | Overlay external context (`KID-CON-0052`) |
| Does path matter? | Structural context (`KID-CON-0042`) |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Two conflicting ranks, no resolution | Analyst confusion |
| OI overrides risk without documentation | Governance gap |
| Risk rank ignores operational reality | Stale priorities |

## Practical implications

When OI and risk rank **conflict**, document resolution in the ticket—precedent for future shifts.

## Limitations

OI reflects operational systems; risk acceptance and compliance may impose parallel requirements.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0034 | [Does OI replace risk analysis?](../faq/FAQ_DOES_OI_REPLACE_RISK_ANALYSIS.md) |

## Authority references

- `KID-OIN-0001` — operational intelligence capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-006 article |
