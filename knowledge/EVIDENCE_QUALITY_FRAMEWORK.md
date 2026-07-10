---
title: "Evidence Quality Framework"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0014
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0010
    - KID-CON-0011
    - KID-CON-0012
    - KID-CON-0013
  related_to:
    - KID-CON-0002
    - KID-CON-0029
    - KID-GLS-0017
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-002]
  difficulty: intermediate
  audience: [analyst, soc_manager, auditor]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0010
    - KID-CON-0013
  recommended_next:
    - KID-CON-0029
    - KID-CON-0027
website_slug: evidence-quality-framework
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "An evidence quality framework evaluates security information across provenance, freshness, confidence, corroboration, specificity, and integrity—supporting consistent investigation and audit-ready decisions."
knowledge_tags: [evidence, quality, education]
---

# Evidence Quality Framework

## What practitioners need to know

Teams need a **shared vocabulary** for grading evidence—not ad hoc "looks good" judgments.

This framework synthesizes dimensions from SER-001 articles into an operational checklist. It does not replace analyst judgment; it **structures** it.

## Quality dimensions

| Dimension | Core question | SER-001 reference |
|-----------|---------------|-------------------|
| **Provenance** | Can origin and handling be traced? | `KID-CON-0011` |
| **Freshness** | Is timing adequate for this decision? | `KID-CON-0012` |
| **Confidence** | How strongly does evidence support the claim? | `KID-CON-0013` |
| **Corroboration** | Do independent sources agree? | `KID-CON-0016` |
| **Specificity** | Is evidence linked to concrete entities? | `KID-GLS-0009`, `KID-GLS-0010` |
| **Integrity** | Was evidence altered or incomplete? | `KID-GLS-0017` |
| **Contradiction handling** | Was disconfirming evidence sought? | `KID-CON-0001` |

## Grading approach

Use **defined tiers** (e.g., high / medium / low) per dimension—not false-precision percentages unless calibrated.

Example pattern for an investigation record:

```text
Claim: Unauthorized admin login on HOST-A
Provenance: High (EDR + IdP logs, query preserved)
Freshness: High (events < 15 minutes)
Confidence: Medium (single user account; MFA status pending)
Corroboration: Medium (two sources; no packet capture)
Action: Continue investigation; do not announce breach externally
```

## Industry context

Quality frameworks appear in forensic science, clinical medicine, and intelligence analysis. Security operations adapted severity and SLA metrics first—quality grading for **analytical** evidence lagged behind.

Mature programs align quality grading with **escalation thresholds**: what quality bar is required for production change, legal hold, or executive notification?

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Scoring only severity | Misaligned escalation |
| One-dimensional "trusted/untrusted" | Lost nuance |
| Quality assessment after decision | Rationalization |
| No team calibration | Inconsistent outcomes |

## Practical implications

1. **Adopt a lightweight rubric** — seven dimensions, three tiers each.  
2. **Calibrate in case reviews** — compare analyst grades on sample cases.  
3. **Tie escalation policy to quality bars** — document explicitly.  
4. **Improve weakest dimensions** — provenance tooling before more alerts.  

See [Evidence Validation](./EVIDENCE_VALIDATION.md) (`KID-CON-0029`) for operational validation steps.

## Limitations

Frameworks do not eliminate uncertainty. Low-quality evidence may still justify exploratory steps. High-quality evidence can be misinterpreted. The framework supports transparency—not automation of conclusions.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0002 | [What Makes Security Evidence Trustworthy](./WHAT_MAKES_SECURITY_EVIDENCE_TRUSTWORTHY.md) |
| KID-GLS-0017 | [Evidence Integrity](../glossary/EVIDENCE_INTEGRITY.md) |
| KID-CON-0027 | [Evidence Prioritization](./EVIDENCE_PRIORITIZATION.md) |

## Authority references

- `KID-INV-0001` — evidence-driven investigation capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
