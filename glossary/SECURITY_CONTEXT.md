---
term: "Security Context"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0003
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0003
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0004
    - KID-GLS-0007
    - KID-GLS-0009
    - KID-GLS-0010
  authority_reference:
    - KID-ARC-0001
    - KID-PLT-0003
canonical_sources:
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Security context is the set of relationships and attributes—asset role, identity privilege, exposure, business impact, threat relevance—that determine whether a finding matters in a specific environment."
---

# Security Context

## Definition

**Security context** is the set of relationships and attributes that determine whether a finding matters in a **specific environment**: asset role, identity privilege, exposure reachability, business impact, control coverage, active threat relevance, and related factors.

A critical vulnerability on an isolated lab system and the same CVE on an internet-facing production identity store are **different decisions** because context differs—not because the CVE identifier changed.

## SentriScope Usage

SentriScope normalizes context through canonical entities (`KID-ARC-0001`) and correlates signals in operational and investigation layers (`KID-OIN-0001`, `KID-INV-0001`). This entry defines the term only.

## Related Terms

- [Risk](./RISK.md) — `KID-GLS-0004`
- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Correlation](./CORRELATION.md) — `KID-GLS-0013`

## Related Knowledge

- [Understanding Security Context](../knowledge/UNDERSTANDING_SECURITY_CONTEXT.md) — `KID-CON-0006`
- [Context Matters More Than Severity](../knowledge/CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) — `KID-CON-0003`
- [FAQ: What is security context?](../faq/FAQ_WHAT_IS_SECURITY_CONTEXT.md) — `KID-FAQ-0005`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging alignment for context-first prioritization |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
