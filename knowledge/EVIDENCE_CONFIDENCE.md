---
title: "Evidence Confidence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0013
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-GLS-0015
    - KID-CON-0002
  explains:
    - KID-GLS-0015
  related_to:
    - KID-CON-0012
    - KID-CON-0014
    - KID-CON-0029
  authority_reference:
    - KID-TIN-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-002]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0002
    - KID-GLS-0015
  recommended_next:
    - KID-CON-0014
    - KID-CON-0029
website_slug: evidence-confidence
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Evidence confidence expresses justified belief in a conclusion given available evidence—not tool severity, alert count, or analyst optimism alone."
knowledge_tags: [evidence, confidence, education]
---

# Evidence Confidence

## What practitioners need to know

**Confidence** is how strongly available evidence supports a conclusion—distinct from **severity**, **priority**, or **urgency**.

Practitioners ask: *How sure are we?* *Is "critical" the same as "confirmed"?*

Term authority: [Evidence Confidence](../glossary/EVIDENCE_CONFIDENCE.md) (`KID-GLS-0015`).

## Confidence vs other labels

| Label | Meaning |
|-------|---------|
| **Severity** | Potential impact if true |
| **Priority** | Order of work given resources |
| **Urgency** | Time sensitivity |
| **Confidence** | Strength of belief given evidence |

A **critical-severity, low-confidence** hypothesis warrants investigation. A **low-severity, high-confidence** finding may warrant immediate targeted fix.

## Factors that raise confidence

- Independent corroboration from unrelated sources  
- Entity linkage (asset, identity) validated  
- Reproducible observation (query replay matches)  
- Consistent timeline across sources  
- Absence of credible contradictory evidence after active search  

## Factors that lower confidence

- Single-source, unvalidated signal  
- Missing provenance or stale state  
- Known false-positive pattern for the rule  
- Contradictory evidence not yet resolved  
- Threat intel without local observation  

## Industry context

Threat intelligence communities use explicit confidence models (e.g., high/medium/low with definitions). Security operations often inherit vendor severity without translating to **analytical confidence**—creating mismatch between executive dashboards and analyst reality.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Equating CVSS or alert priority with confidence | Wrong escalation |
| Never documenting low-confidence assumptions | Audit failure |
| Confidence inflation after alert duplication | False certainty |
| Ignoring TI confidence ratings | Over-reliance on third-party claims |

## Practical implications

1. **State confidence explicitly** in investigation records.  
2. **List what would raise or lower confidence** (pre-mortem style).  
3. **Separate confidence from action** — low confidence may still require containment when stakes are high.  
4. **Align language** across SOC, IR, and leadership.  

Threat intelligence confidence concepts: `KID-TIN-0001` (product authority—not redefined here).

## Limitations

Confidence is not probability unless teams define calibrated scales. Forced numeric scores without methodology create false precision. Qualitative, defined tiers often serve operational teams better.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0015 | [Evidence Confidence](../glossary/EVIDENCE_CONFIDENCE.md) |
| KID-CON-0002 | [What Makes Security Evidence Trustworthy](./WHAT_MAKES_SECURITY_EVIDENCE_TRUSTWORTHY.md) |
| KID-CON-0029 | [Evidence Validation](./EVIDENCE_VALIDATION.md) |
| KID-FAQ-0008 | [How do you validate security evidence?](../faq/FAQ_HOW_TO_VALIDATE_SECURITY_EVIDENCE.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
