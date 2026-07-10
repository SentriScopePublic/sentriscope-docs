---
term: "Investigation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0002
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0002
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
  related_to:
    - KID-GLS-0003
    - KID-GLS-0011
  authority_reference:
    - KID-INV-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_SESSION_PLATFORM.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "A security investigation is a structured, analyst-led process of gathering evidence, forming hypotheses, and reaching validated conclusions—not the same as incident response or alert triage alone."
---

# Investigation

## Definition

A **security investigation** is a structured, analyst-led process of gathering **evidence**, forming and testing hypotheses, and reaching **validated conclusions** about a security question. Investigations may span hours or weeks and often pause and resume across tools and teams.

Investigation is **not** identical to incident response (which emphasizes containment and recovery) or to single-alert triage (which may stop at disposition without preserved reasoning).

## SentriScope Usage

SentriScope supports persistent investigation sessions with evidence, findings, and analyst validation. Capability scope: `KID-INV-0001`. Boundaries (not autonomous closure): `KID-PLT-0002`.

## Related Terms

- [Evidence](./EVIDENCE.md) — `KID-GLS-0001`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`

## Related Knowledge

- [Evidence-Based Investigation](../knowledge/EVIDENCE_BASED_INVESTIGATION.md) — `KID-CON-0001`
- [Security Investigation vs Incident Response](../knowledge/SECURITY_INVESTIGATION_VS_INCIDENT_RESPONSE.md) — `KID-CON-0005`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INVESTIGATION_SESSION_PLATFORM.md` | Investigation session concepts |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
