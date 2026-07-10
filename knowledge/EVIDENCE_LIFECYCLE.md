---
title: "Evidence Lifecycle"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0015
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-CON-0011
    - KID-CON-0012
  related_to:
    - KID-CON-0018
    - KID-GLS-0016
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-004]
  difficulty: intermediate
  audience: [analyst, auditor]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0011
    - KID-CON-0012
  recommended_next:
    - KID-CON-0018
    - KID-CON-0016
website_slug: evidence-lifecycle
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "The evidence lifecycle spans discovery, collection, validation, analysis, decision use, retention, and disposition—each stage affecting quality, freshness, and audit defensibility."
knowledge_tags: [evidence, lifecycle, education]
---

# Evidence Lifecycle

## What practitioners need to know

Evidence is not static. It moves through **stages**—each with different quality requirements and risks.

Practitioners ask: *When do we collect?* *How long do we keep it?* *When is it no longer valid?*

## Lifecycle stages

| Stage | Description | Primary risk if neglected |
|-------|-------------|---------------------------|
| **Discovery** | Potential evidence identified (alert, hunt hit) | Wrong scope |
| **Collection** | Data captured with provenance | Loss, tampering |
| **Validation** | Authenticity and relevance checked | False conclusions |
| **Analysis** | Linked to hypotheses and entities | Confirmation bias |
| **Decision use** | Supports or contradicts action | Overreach |
| **Retention** | Stored per policy | Spoliation, cost |
| **Disposition** | Archived or destroyed per rules | Legal exposure |

## Industry context

Legal hold and regulatory retention intersect security evidence lifecycles—especially after incidents. Teams that treat logs as infinite and free often discover retention gaps only during discovery.

[Chain of custody](../glossary/CHAIN_OF_CUSTODY.md) (`KID-GLS-0016`) applies across collection through disposition for high-stakes matters.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Collecting everything, validating nothing | Storage cost; no insight |
| Deleting sources before investigation closes | Cannot reproduce |
| No retention alignment with legal | Spoliation risk |
| Skipping validation under time pressure | Wrong containment |

## Practical implications

1. **Define lifecycle policies** by evidence class (telemetry, exports, analyst notes).  
2. **Automate collection metadata** at ingest where possible.  
3. **Gate high-impact decisions** on validation stage completion.  
4. **Coordinate with legal/compliance** on hold triggers.  

See [Evidence in Audit and Compliance](./EVIDENCE_IN_AUDIT_AND_COMPLIANCE.md) (`KID-CON-0018`).

## Limitations

Not all evidence requires full lifecycle rigor. Match process to stakes. Lightweight incidents may use abbreviated paths—document the choice.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0011 | [Evidence Provenance](./EVIDENCE_PROVENANCE.md) |
| KID-CON-0012 | [Evidence Freshness](./EVIDENCE_FRESHNESS.md) |
| KID-GLS-0016 | [Chain of Custody](../glossary/CHAIN_OF_CUSTODY.md) |
| KID-CON-0029 | [Evidence Validation](./EVIDENCE_VALIDATION.md) |

## Authority references

- `KID-INV-0001` — persistent investigation and evidence packages

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
