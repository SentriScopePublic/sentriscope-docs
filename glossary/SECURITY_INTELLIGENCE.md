---
term: "Security Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0028
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0028
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0005
    - KID-GLS-0006
    - KID-GLS-0023
    - KID-GLS-0024
  explains:
    - KID-CON-0070
  authority_reference:
    - KID-TIN-0001
    - KID-OIN-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Security intelligence is the integrated use of external threat knowledge and internal operational knowledge—alongside evidence and risk context—to support explainable security decisions."
---

# Security Intelligence

## Definition

**Security intelligence** is the **integrated application** of external **threat intelligence** and internal **operational intelligence**—correlated with **evidence**, **risk context**, and **investigation state**—to produce **explainable decision support** for prioritization, investigation scope, and stakeholder communication.

Security intelligence is not a third feed category. It is the **operating discipline** of combining intelligence types without letting any single source override validated evidence or accountable risk judgment.

## Distinction from component intelligence types

| Dimension | Threat Intelligence | Operational Intelligence | Security Intelligence |
|-----------|--------------------|--------------------------|------------------------|
| **Scope** | External environment | Internal organization state | **Integrated decision process** |
| **Primary question** | What threats matter now? | Where should we focus internally? | **What should we decide—and why?** |
| **Inputs** | Reports, campaigns, indicators | Assets, telemetry, queues, controls | **TI + OI + evidence + risk** |
| **Output** | Contextual external hypotheses | Explainable internal rank | **Unified, auditable recommendations** |

## Related Terms

- [Threat Intelligence](./THREAT_INTELLIGENCE.md) — `KID-GLS-0005`
- [Operational Intelligence](./OPERATIONAL_INTELLIGENCE.md) — `KID-GLS-0006`
- [Decision Support](./DECISION_SUPPORT.md) — `KID-GLS-0023`
- [Intelligence Confidence](./INTELLIGENCE_CONFIDENCE.md) — `KID-GLS-0024`

## Related Knowledge

- [Understanding Security Intelligence](../knowledge/UNDERSTANDING_SECURITY_INTELLIGENCE.md) — `KID-CON-0070`
- [SER-007 Security Intelligence](../knowledge/SERIES_007_SECURITY_INTELLIGENCE.md)
- [Threat Intelligence as Decision Support](../knowledge/THREAT_INTELLIGENCE_AS_DECISION_SUPPORT.md) — `KID-CON-0058`
- [Operational Intelligence as Decision Support](../knowledge/OPERATIONAL_INTELLIGENCE_AS_DECISION_SUPPORT.md) — `KID-CON-0068`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | Intelligence integration model (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-007) |
