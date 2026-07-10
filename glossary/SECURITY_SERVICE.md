---
term: "Security Service"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0034
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0034
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0033
    - KID-GLS-0009
    - KID-GLS-0003
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security service is an exposed capability or API endpoint that carries security significance distinct from the hosting application—often the technical unit logs and scanners name, enriched and mapped to application scope."
---

# Security Service

## Definition

A **security service** is an **exposed capability or API endpoint** that carries **security significance** distinct from the hosting [security application](./SECURITY_APPLICATION.md).

Services are often the **technical delivery units** analysts encounter in logs, vulnerability findings, and monitoring—named endpoints, hosted workloads, SaaS instances, or internal APIs. They matter for enrichment and containment detail, but **business scope and stakeholder narrative** attach to the application boundary, not to every service record in isolation.

## SentriScope Usage

SentriScope maps services to canonical applications (`KID-ARC-0001`) so analysts can scope investigations and communicate impact at the business-capability level. This entry defines the term only.

## Related terms

- [Security Application](./SECURITY_APPLICATION.md) — `KID-GLS-0033`
- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-010) |
