---
term: "Asset Criticality"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0029
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0029
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0009
    - KID-GLS-0003
    - KID-GLS-0004
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Asset criticality is the business and security significance of an asset that changes how findings, vulnerabilities, and incidents are prioritized—not merely inventory classification."
---

# Asset Criticality

## Definition

**Asset criticality** is the **business and security significance** of an [asset](./ASSET.md) that **changes how findings, vulnerabilities, and incidents are prioritized**.

Criticality reflects **context**—what the asset supports, who depends on it, and what harm could follow from compromise—not label hygiene in a CMDB alone.

## SentriScope Usage

SentriScope enriches canonical assets with criticality signals from business and security context (`KID-ARC-0001`) so prioritization and intelligence layers can explain **why** the same finding ranks differently on different assets. This entry defines the term only.

## Related terms

- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Risk](./RISK.md) — `KID-GLS-0004`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-008) |
