---
title: "Investigation Decisions"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0023
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0013
    - KID-CON-0020
    - KID-CON-0021
  related_to:
    - KID-CON-0008
    - KID-CON-0024
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-002
  editorial_season: SEA-001
  pillar_page: PIL-INVESTIGATION
  learning_path: LP-002
  search_intent_ids: [SI-015]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0020
    - KID-CON-0013
  recommended_next:
    - KID-CON-0008
    - KID-CON-0025
website_slug: investigation-decisions
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Investigation decisions—escalate, contain, close, or defer—require explicit confidence, evidence linkage, and documented rationale aligned with decision stakes."
knowledge_tags: [investigation, decisions, education]
---

# Investigation Decisions

## What practitioners need to know

Investigations produce **decisions**: escalate, contain, remediate, accept risk, close as benign, or defer pending evidence.

Practitioners ask: *When is it safe to close?* *When must we escalate despite incomplete evidence?*

## Decision types

| Decision | Typical trigger | Evidence bar |
|----------|-----------------|--------------|
| **Close (benign)** | Hypothesis refuted | Medium — document negative searches |
| **Close (resolved)** | Issue fixed; scope known | High for repeat-risk cases |
| **Escalate to IR** | Active harm likely | Medium-high; bias toward safety |
| **Escalate to leadership** | Business/regulatory impact | High documentation |
| **Defer** | Missing evidence; low immediate risk | Explicit revisit time |
| **Accept risk** | Known gap; business accepts | Formal risk record |

## Confidence and stakes

Use [evidence confidence](./EVIDENCE_CONFIDENCE.md) (`KID-CON-0013`) explicitly:

- **High stakes + low confidence** → escalate or contain while investigating  
- **Low stakes + medium confidence** → remediate with monitoring  
- **Any stakes + high confidence contradictory evidence** → close with learning  

Decisions are not binary with alert severity.

## Industry context

Runbooks often prescribe actions by alert type; evidence-based programs prescribe actions by **validated scope and confidence**. Post-incident reviews frequently cite decisions made on intuition under SLA pressure.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Closing to meet SLA | Repeat incidents |
| Escalating every uncertain case | IR fatigue |
| No decision record | Audit and learning failure |
| Deferred forever | Silent risk acceptance |

## Practical implications

1. **Template decision records**: claim, confidence, evidence KIDs, action, owner.  
2. **Define escalation matrix** by asset tier and confidence gap.  
3. **Separate disposition** (alert handled) from **investigation outcome**.  
4. **Schedule deferred revisits** with calendar triggers.  

See [From Alerts to Decisions](./FROM_ALERTS_TO_DECISIONS.md) (`KID-CON-0008`).

## Limitations

Perfect certainty is rare. Document **residual uncertainty** when acting—especially for containment decisions.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0008 | [From Alerts to Decisions](./FROM_ALERTS_TO_DECISIONS.md) |
| KID-GLS-0019 | [Disposition](../glossary/DISPOSITION.md) |
| KID-FAQ-0015 | [When should an investigation be escalated?](../faq/FAQ_WHEN_ESCALATE_INVESTIGATION.md) |

## Authority references

- `KID-INV-0001` — investigation outcomes and analyst validation

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-002 article |
