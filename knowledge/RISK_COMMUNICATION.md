---
title: "Risk Communication"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0033
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0031
    - KID-CON-0035
  related_to:
    - KID-CON-0032
    - KID-CON-0023
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-003
  editorial_season: SEA-005
  pillar_page: PIL-RISK
  learning_path: LP-003
  search_intent_ids: [SI-061]
  difficulty: intermediate
  audience: [analyst, soc_manager, ciso, executive]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0031
  recommended_next:
    - KID-CON-0032
website_slug: risk-communication
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Risk communication translates explainable prioritization into stakeholder language—impact, context, confidence, and recommended action—without jargon dumps or raw severity counts."
knowledge_tags: [risk, communication, education]
---

# Risk Communication

## What practitioners need to know

Practitioners ask: *How do I explain prioritization to leadership?* *Why don't executives trust the VM report?*

**Risk communication** translates **explainable prioritization** into language stakeholders act on—without CVSS dumps or alert volume metrics.

## Audience-specific framing

| Audience | Needs | Avoid |
|----------|-------|-------|
| **Executives** | Business impact, decision, resource ask | CVE lists, tool jargon |
| **Application owners** | Specific asset, fix window, consequence | Global severity stats |
| **Auditors** | Evidence, rationale, acceptance records | "We use best practices" |
| **SOC peers** | Context, evidence KIDs, next steps | Ambiguous "high risk" |

## Communication structure

1. **Situation** — what finding or theme  
2. **Context** — exposure, asset tier, threat (`KID-CON-0030`)  
3. **Evidence confidence** — validated vs assumed  
4. **Risk rank rationale** — why now, why first  
5. **Recommended action** — fix, accept, investigate  
6. **Uncertainty** — what we do not yet know  

## Industry context

Executive dashboards showing "500 Critical open" destroy trust. Dashboards showing **top 5 explainable business risks with owners** enable action—core to risk intelligence, not fear marketing.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Severity-only slides | Wrong resource allocation |
| No recommended action | Meeting without decision |
| Hiding uncertainty | Surprise when wrong |
| Different story to audit vs ops | Credibility loss |

## Practical implications

1. **Use rank templates** with business context fields.  
2. **Lead with impact**, support with technical detail in appendix.  
3. **Align with investigation documentation** standards (`KID-CON-0026`).  
4. **Review messaging** after major incidents for calibration.  

## Limitations

Stakeholders may still demand "fix all Criticals." Document trade-offs and acceptance paths (`KID-CON-0032`) rather than overpromise.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0035 | [Business Context in Risk Decisions](./BUSINESS_CONTEXT_IN_RISK_DECISIONS.md) |
| KID-FAQ-0019 | [How do analysts explain risk to executives?](../faq/FAQ_HOW_ANALYSTS_EXPLAIN_RISK.md) |

## Authority references

- `KID-OIN-0001` — operational views for stakeholder communication

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-003 article |
