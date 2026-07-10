---
title: "Evidence Prioritization"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0027
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0014
    - KID-GLS-0004
    - KID-GLS-0003
  related_to:
    - KID-CON-0003
    - KID-CON-0016
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-008]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0014
  recommended_next:
    - KID-CON-0003
website_slug: evidence-prioritization
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Evidence prioritization ranks which observations deserve analyst attention next—using quality, context, and decision stakes—not alert severity or volume alone."
knowledge_tags: [evidence, prioritization, education]
---

# Evidence Prioritization

## What practitioners need to know

Teams face more observations than capacity. **Prioritization** decides what to examine next—not what is true.

Practitioners ask: *Which evidence do I dig into first?* *Is critical severity enough?*

## Prioritization inputs

| Input | Role |
|-------|------|
| **Evidence quality** | Low-quality items may wait for enrichment |
| **Security context** | Business exposure, asset criticality (`KID-GLS-0003`) |
| **Confidence gap** | High-impact + low-confidence → urgent validation |
| **Freshness** | Time-sensitive incidents weight recent evidence |
| **Corroboration** | Strong multi-source signals may jump queue |
| **Decision stakes** | Regulatory, safety, revenue impact |

Severity from tools is **one input**, not the ranking function.

## Industry context

Operational intelligence programs exist to improve prioritization under overload—see `KID-OIN-0001`. Traditional SOC queues sorted by severity alone remain a common anti-pattern.

[Risk](../glossary/RISK.md) (`KID-GLS-0004`) contextualizes impact; [Context Matters More Than Severity](./CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) (`KID-CON-0003`) extends this theme.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| FIFO only | Critical items buried |
| Severity-only sorting | Context-blind response |
| Never reprioritizing | Stale queue |
| Prioritizing duplicates as separate work | Wasted capacity |

## Practical implications

1. **Define prioritization rubric** aligned with evidence quality framework.  
2. **Re-score on new evidence** — queues are dynamic.  
3. **Cap concurrent deep dives** — finish validation loops.  
4. **Measure outcome quality**, not only queue drain rate.  

## Limitations

Prioritization errors are inevitable under uncertainty. Document deferred items with rationale—"not ignored; deprioritized because…"

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0014 | [Evidence Quality Framework](./EVIDENCE_QUALITY_FRAMEWORK.md) |
| KID-CON-0003 | [Context Matters More Than Severity](./CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) |
| KID-GLS-0003 | [Security Context](../glossary/SECURITY_CONTEXT.md) |

## Authority references

- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
