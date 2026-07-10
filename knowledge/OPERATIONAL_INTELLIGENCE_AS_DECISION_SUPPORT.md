---
title: "Operational Intelligence as Decision Support"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0068
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0060
    - KID-CON-0066
    - KID-GLS-0023
  synthesizes:
    - KID-CON-0060
    - KID-CON-0061
    - KID-CON-0062
    - KID-CON-0063
    - KID-CON-0064
    - KID-CON-0065
    - KID-CON-0066
    - KID-CON-0067
  related_to:
    - KID-CON-0058
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-006
  pillar_page: PIL-OP-INTEL
  learning_path: LP-006
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0066
  recommended_next:
    - KID-CON-0070
website_slug: operational-intelligence-as-decision-support
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Synthesis: organizations transform operational knowledge into better security decisions through explainable internal prioritization—not SIEM operations or autonomous SOC."
knowledge_tags: [operational-intelligence, decision-support, education]
---

# Operational Intelligence as Decision Support

## Core thesis

Organizations transform **operational knowledge** into **better security decisions** by making internal state **explainable and actionable**—not by collecting more logs.

## Decision-support model

```text
Internal operational data + Operational context
              ↓
   Operational intelligence (explainable rank)
              ↓
        Better security decisions
```

| Principle | Meaning |
|-----------|---------|
| **OI is internal** | Complements external TI (`KID-CON-0058`) |
| **OI is not data** | Rank with reasons (`KID-CON-0061`) |
| **OI is not SIEM ops** | Decision support, not query tutorials |
| **OI feeds investigation & risk** | `KID-CON-0065`, `KID-CON-0066` |
| **OI requires context** | `KID-CON-0063`, `KID-GLS-0027` |
| **OI has limits** | `KID-CON-0067` |

## Volume 2 position

```text
SER-005 Threat Intelligence     → external knowledge → decisions
SER-006 Operational Intelligence → internal knowledge → decisions
SER-007 Security Intelligence    → unified integration (next)
```

## Operating checklist

1. ☐ Is rank explainable to another analyst?  
2. ☐ Is operational context current?  
3. ☐ Does risk/TI context agree or conflict—documented?  
4. ☐ Is evidence required before irreversible action?  
5. ☐ Is residual operational risk stated?  

## Practical implications

Prepare for **SER-007** by identifying where TI and OI ranks diverge today—integration work starts there.

## Authority references

- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)
- `KID-GLS-0023` — [Decision Support](../glossary/DECISION_SUPPORT.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-006 synthesis article |
