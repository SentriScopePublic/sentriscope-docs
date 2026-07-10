---
title: "Investigation Quality"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0021
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0014
    - KID-CON-0019
    - KID-CON-0020
  related_to:
    - KID-CON-0022
    - KID-CON-0026
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-002
  editorial_season: SEA-001
  pillar_page: PIL-INVESTIGATION
  learning_path: LP-002
  search_intent_ids: [SI-014]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0019
    - KID-CON-0014
  recommended_next:
    - KID-CON-0023
    - KID-CON-0026
website_slug: investigation-quality
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Investigation quality measures whether an inquiry used structured lifecycle, validated evidence, explicit hypotheses, and documented reasoning—not merely whether tickets closed quickly."
knowledge_tags: [investigation, quality, education]
---

# Investigation Quality

## What practitioners need to know

**Investigation quality** is whether the inquiry produced **defensible conclusions** through structured process—not whether the ticket closed within SLA.

Practitioners ask: *How do we measure good investigations?* *Why do repeat incidents happen after "closed" cases?*

## Quality dimensions

| Dimension | Indicator of quality |
|-----------|---------------------|
| **Scope clarity** | Boundaries documented |
| **Hypothesis discipline** | Explicit, tested claims |
| **Evidence quality** | Provenance, validation (`KID-CON-0014`) |
| **Contradiction handling** | Disconfirming evidence sought |
| **Decision linkage** | Actions trace to evidence |
| **Documentation** | Reproducible by another analyst |
| **Outcome clarity** | Question answered or escalated with reason |

## Quality vs speed

| Metric | Measures | Risk if alone |
|--------|----------|---------------|
| MTTR / time to close | Speed | Superficial closure |
| Reopen rate | Initial quality gap | Hidden rework |
| Repeat incident rate | Root cause quality | Failed learning |
| Audit sample pass rate | Defensibility | Regulatory exposure |

Balance speed with **quality gates** at lifecycle phase transitions (`KID-CON-0019`).

## Industry context

SOC KPIs historically emphasized volume and closure time. Insurance, regulators, and internal audit increasingly sample **investigation records**—not alert counts.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Quality = senior analyst intuition | Inconsistent outcomes |
| No peer review on high-stakes cases | Single point of failure |
| Copy-paste closures | Audit failure |
| Ignoring quality on "low" alerts | Missed precursors |

## Practical implications

1. **Define a lightweight quality rubric** aligned with lifecycle phases.  
2. **Sample investigations monthly** for calibration.  
3. **Track repeat incidents** linked to prior case IDs.  
4. **Reward documented reasoning**, not only queue speed.  

## Limitations

Quality assessment is partly subjective until teams calibrate rubrics. Perfect quality on every alert is economically infeasible—tier rigor by asset criticality and decision stakes.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0022 | [Investigation Bias](./INVESTIGATION_BIAS.md) |
| KID-CON-0026 | [Investigation Documentation](./INVESTIGATION_DOCUMENTATION.md) |
| KID-CON-0001 | [Evidence-Based Investigation](./EVIDENCE_BASED_INVESTIGATION.md) |

## Authority references

- `KID-INV-0001` — investigation session quality and evidence governance

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-002 article |
