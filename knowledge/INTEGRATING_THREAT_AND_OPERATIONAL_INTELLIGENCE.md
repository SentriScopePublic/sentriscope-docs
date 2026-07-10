---
title: "Integrating Threat and Operational Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0071
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0070
    - KID-GLS-0005
    - KID-GLS-0006
    - KID-GLS-0013
  related_to:
    - KID-CON-0073
    - KID-CON-0074
  authority_reference:
    - KID-TIN-0001
    - KID-OIN-0001
navigation:
  knowledge_series: SER-007
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0070
  recommended_next:
    - KID-CON-0072
website_slug: integrating-threat-and-operational-intelligence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Integration means correlating external threat context with internal operational state to produce reconciled, explainable priorities—not running TI and OI as parallel silos."
knowledge_tags: [security-intelligence, threat-intelligence, operational-intelligence, education]
---

# Integrating Threat and Operational Intelligence

## What practitioners need to know

Integration fails when teams **consume TI and OI separately** and discover conflicting priorities at escalation time. Effective integration **correlates** external threat relevance with internal operational state **before** decisions reach stakeholders.

## Integration vs parallel consumption

| Parallel (fails) | Integrated (succeeds) |
|------------------|-------------------------|
| TI team publishes; SOC ignores until urgent | TI mapped to affected assets and identities |
| OI rank ignores active campaigns | Campaign context elevates relevant internal signals |
| Separate dashboards, separate meetings | Single reconciled priority with reason codes |
| Conflicts resolved ad hoc | Documented reconciliation rules |

## Correlation workflow

```text
1. External signal (campaign, exploitation, TTP)
        ↓
2. Map to internal inventory (assets, identities, exposures)
        ↓
3. Cross-check operational rank and queue state
        ↓
4. Reconcile: elevate, hold, or de-prioritize with rationale
        ↓
5. Record intelligence inputs used in decision
```

[Correlation](../glossary/CORRELATION.md) (`KID-GLS-0013`) is the mechanism; security intelligence is the **operating outcome**.

## Reconciliation patterns

| Situation | Integration response |
|-----------|---------------------|
| TI urgent, OI shows no exposure | De-prioritize with documented gap—or hunt for blind spots |
| OI urgent, TI silent | Proceed on internal evidence; note absence of external context |
| Both urgent, same asset | Escalate with combined rationale |
| TI and OI disagree on asset | Investigate mapping accuracy first |
| Stale TI, fresh OI | Weight timeliness; refresh external context |

## Roles in integration

| Role | Integration responsibility |
|------|---------------------------|
| **Analyst** | Apply reconciliation at triage and investigation |
| **Intel curator** | Maintain relevance mapping and confidence |
| **Risk owner** | Accept residual risk when intelligence conflicts |
| **SOC manager** | Enforce single priority narrative per item |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Integration = single vendor platform | Process gap remains |
| Correlation without inventory accuracy | False relevance |
| TI always wins over OI | Internal blind spots ignored |
| OI always wins over TI | Campaign exposure missed |
| No conflict documentation | Unauditable decisions |

## Practical implications

1. **Define reconciliation rules** before the next major campaign.  
2. **Require both intelligence types cited** (or explicit "not applicable") in escalation records.  
3. **Review weekly** where TI and OI ranks diverged by more than one tier.  

## Limitations

Integration cannot compensate for missing asset inventory, poor TI curation, or operational data gaps—fix foundations before automating reconciliation.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0037 | [How do TI and OI work together?](../faq/FAQ_HOW_TI_AND_OI_WORK_TOGETHER.md) |
| KID-CON-0053 | [Context Matters in Threat Intelligence](./CONTEXT_MATTERS_IN_THREAT_INTELLIGENCE.md) |
| KID-CON-0063 | [Why Context Changes Operational Decisions](./WHY_CONTEXT_CHANGES_OPERATIONAL_DECISIONS.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)
- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 article |
