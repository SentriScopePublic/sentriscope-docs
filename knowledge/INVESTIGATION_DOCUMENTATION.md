---
title: "Investigation Documentation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0026
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0001
    - KID-CON-0011
    - KID-CON-0019
  related_to:
    - KID-CON-0025
    - KID-CON-0018
    - KID-CON-0021
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-002
  editorial_season: SEA-001
  pillar_page: PIL-INVESTIGATION
  learning_path: LP-002
  search_intent_ids: [SI-018]
  difficulty: intermediate
  audience: [analyst, auditor]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0019
    - KID-CON-0011
  recommended_next:
    - KID-CON-0025
    - KID-CON-0018
website_slug: investigation-documentation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Investigation documentation captures scope, hypotheses, evidence with provenance, analysis, decisions, and outcomes so another analyst or auditor can reproduce the reasoning path."
knowledge_tags: [investigation, documentation, education]
---

# Investigation Documentation

## What practitioners need to know

**Documentation** is how investigations survive handoff, audit, and time. Without it, conclusions exist only in memory.

Practitioners ask: *What should I write down?* *How much is enough?*

## What to document

| Section | Content |
|---------|---------|
| **Trigger** | Alert, hunt, executive ask, audit finding |
| **Scope** | Boundaries and exclusions |
| **Hypotheses** | Active and retired (`KID-CON-0020`) |
| **Evidence log** | Items with provenance (`KID-CON-0011`) |
| **Analysis notes** | Correlation, contradiction handling |
| **Confidence** | Tier and justification (`KID-CON-0013`) |
| **Decisions** | Actions with rationale (`KID-CON-0023`) |
| **Outcome** | Question answered? Residual risk? |
| **Disposition** | Alert/ticket status (`KID-GLS-0019`) |

## Documentation tiers

| Tier | When | Minimum content |
|------|------|-----------------|
| **Light** | Benign quick close | Trigger, negative search, disposition |
| **Standard** | Typical SOC case | Hypothesis + key evidence + outcome |
| **Full** | Incident, legal, regulatory | Complete package + chain of custody |

Match tier to stakes—see [Evidence in Audit and Compliance](./EVIDENCE_IN_AUDIT_AND_COMPLIANCE.md) (`KID-CON-0018`).

## Industry context

Regulators and insurers request investigation records—not SIEM dashboards. Teams that document during work avoid painful reconstruction under deadline.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Post-hoc documentation | Rationalization bias |
| Screenshots without queries | Non-reproducible |
| Narrative without evidence links | Unverifiable |
| Over-documenting noise | Analyst burnout |

## Practical implications

1. **Use templates** aligned to lifecycle phases.  
2. **Link evidence by stable reference** (KID, source query ID).  
3. **Document negative searches**—what you looked for and did not find.  
4. **Time-box documentation** as part of closure criteria.  

## Limitations

Documentation is not a substitute for quality analysis—but absence guarantees future failure on review and learning.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0021 | [Investigation Quality](./INVESTIGATION_QUALITY.md) |
| KID-GLS-0019 | [Disposition](../glossary/DISPOSITION.md) |
| KID-FAQ-0014 | [How do you document an investigation?](../faq/FAQ_HOW_TO_DOCUMENT_INVESTIGATION.md) |

## Authority references

- `KID-INV-0001` — investigation session documentation

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-002 article |
