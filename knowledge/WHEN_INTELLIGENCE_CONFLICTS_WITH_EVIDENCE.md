---
title: "When Intelligence Conflicts With Evidence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0076
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0029
    - KID-CON-0070
    - KID-GLS-0001
    - KID-GLS-0024
  related_to:
    - KID-CON-0074
    - KID-CON-0075
  authority_reference:
    - KID-GLS-0028
navigation:
  knowledge_series: SER-007
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0070
    - KID-CON-0029
  recommended_next:
    - KID-CON-0077
website_slug: when-intelligence-conflicts-with-evidence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "When intelligence conflicts with evidence, evidence leads investigation conclusions—intelligence is revised, scoped, or held pending validation, never silently overriding ground truth."
knowledge_tags: [security-intelligence, evidence, education]
---

# When Intelligence Conflicts With Evidence

## What practitioners need to know

Conflicts between intelligence and evidence are **normal**—they signal mapping errors, stale reporting, or incomplete collection. **Evidence leads** investigation conclusions; intelligence **adapts** when ground truth disagrees.

Anchor on [Evidence](../glossary/EVIDENCE.md) (`KID-GLS-0001`) and [Evidence Validation](./EVIDENCE_VALIDATION.md) (`KID-CON-0029`).

## Hierarchy of trust

```text
Validated evidence (highest for "what happened")
        ↓
Risk context (business judgment)
        ↓
Integrated intelligence (hypothesis and urgency)
        ↓
Unvalidated intelligence (lowest—hold action)
```

Intelligence **never silently overrides** validated evidence. When they conflict, **investigate the conflict** before escalating irreversible action.

## Common conflict patterns

| Conflict | Likely cause | Response |
|----------|--------------|----------|
| TI IoC match, no telemetry | False positive, wrong asset mapping | Refine scope; do not declare breach |
| Evidence of technique, TI silent | Local variant, stale feeds | Hunt with evidence; refresh TI |
| OI high rank, evidence clean | Compensating control, stale finding | Reconcile OI; document control |
| TI campaign urgent, no internal exposure | Sector noise, mapping gap | Verify inventory; proportionate response |
| Intelligence confident, evidence immature | Premature escalation pressure | State uncertainty; continue collection |

## Resolution workflow

1. **Document the conflict** in investigation or prioritization record.  
2. **Prefer evidence** for factual conclusions (what occurred).  
3. **Re-evaluate intelligence** relevance, confidence, and mapping.  
4. **Communicate uncertainty** to stakeholders (`KID-CON-0075`).  
5. **Feed back** to TI curation and OI tuning.  

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Intelligence wins because "classified" | Wrong conclusions |
| Ignoring conflict to close ticket | Latent exposure |
| Discarding TI when one IoC fails | Missed broader campaign |
| No conflict in audit trail | Unexplainable decisions |
| Treating absence of evidence as proof of safety | False negative closure |

## Practical implications

1. **Add conflict field** to triage and investigation templates.  
2. **Train analysts**: conflict is signal, not failure.  
3. **Review monthly** conflicts that led to rank changes.  

## Limitations

Evidence can be incomplete or stale too—conflict resolution requires **collection investment**, not arbitrary tie-breaking rules favoring either side without investigation.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0038 | [Can intelligence override evidence?](../faq/FAQ_CAN_INTELLIGENCE_OVERRIDE_EVIDENCE.md) |
| KID-CON-0013 | [Evidence Confidence](./EVIDENCE_CONFIDENCE.md) |
| KID-CON-0057 | [When Threat Intelligence Is Not Enough](./WHEN_THREAT_INTELLIGENCE_IS_NOT_ENOUGH.md) |

## Authority references

- `KID-GLS-0028` — [Security Intelligence](../glossary/SECURITY_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 article |
