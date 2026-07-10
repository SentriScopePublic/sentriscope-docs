---
term: "Threat Indicator"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0025
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0025
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0005
    - KID-GLS-0008
  explains:
    - KID-CON-0051
  authority_reference:
    - KID-TIN-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A threat indicator is an observable artifact associated with threat activity—such as a hash, domain, or IP—used as decision-support input after contextual validation, not as standalone proof of compromise."
---

# Threat Indicator

## Definition

A **threat indicator** (often **IoC**—indicator of compromise) is an **observable artifact** associated with threat activity—such as a file hash, domain, IP address, or email pattern.

Indicators are **inputs to investigation and prioritization**. A match suggests **where to look**; it is not synonymous with a [Finding](./FINDING.md) (`KID-GLS-0008`) or proof of active compromise until validated with evidence.

## Usage discipline

| Indicator match means | Indicator match does not mean |
|-----------------------|-------------------------------|
| Hunt or investigate | Incident declared |
| Possible relevance | Automatic remediation |
| Hypothesis trigger | Replacement for risk analysis |

## Related terms

- [Threat Intelligence](./THREAT_INTELLIGENCE.md) — `KID-GLS-0005`
- [Finding](./FINDING.md) — `KID-GLS-0008`

## Related knowledge

- [Threat Intelligence vs Detection](../knowledge/THREAT_INTELLIGENCE_VS_DETECTION.md) — `KID-CON-0051`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-005) |
