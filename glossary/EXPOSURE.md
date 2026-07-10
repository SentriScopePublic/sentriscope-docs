---
term: "Exposure"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0007
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0007
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0008
    - KID-GLS-0009
    - KID-GLS-0004
  authority_reference:
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
publication_phase: phase_2
website_slug: glossary-exposure
last_updated: 2026-07-07
next_review: 2027-01-07
llm_summary: "An exposure is a security finding that links an asset or related entity to a vulnerability or exposure condition in a specific environment—not the vulnerability identifier alone."
---

# Exposure

## Definition

An **exposure** is a security finding that links an **asset** (or related entity) to a **vulnerability** or exposure condition **in a specific environment**. The same CVE may produce many exposures across assets; remediation and risk depend on which exposures exist where.

Exposure is not interchangeable with vulnerability catalog entries (for example CVE records) or with generic "issues" without entity linkage.

## SentriScope Usage

Exposure is a canonical entity concept: `KID-ARC-0001`. Data sources feeding exposures: `KID-INT-0001`.

## Related Terms

- [Finding](./FINDING.md) — `KID-GLS-0008`
- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Risk](./RISK.md) — `KID-GLS-0004`

## Related Knowledge

- [Context Matters More Than Severity](../knowledge/CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) — `KID-CON-0003`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Exposure concept (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
