---
term: "Risk"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0004
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0004
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0003
    - KID-GLS-0007
    - KID-GLS-0008
  authority_reference:
    - KID-ARC-0001
    - KID-PLT-0004
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
publication_phase: phase_2
website_slug: glossary-risk
last_updated: 2026-07-07
next_review: 2027-01-07
llm_summary: "In security operations, risk is the prioritized outcome of combining findings with context—likelihood, impact, and threat relevance—not a raw severity score in isolation."
---

# Risk

## Definition

In security operations, **risk** is a **prioritized outcome** that combines findings with **context**: likelihood of exploitation, impact if realized, threat relevance, and control coverage. Risk answers *what should we address first and why*—not merely *what is severe on a generic scale*.

Risk is distinct from raw CVSS or scanner severity, which describe a finding in isolation.

## SentriScope Usage

SentriScope derives deterministic, explainable risk outcomes from canonical inputs (`KID-ARC-0001`). Implementation maturity: `KID-PLT-0004`. This entry does not describe scoring mechanics.

## Related Terms

- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Finding](./FINDING.md) — `KID-GLS-0008`
- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`

## Related Knowledge

- [Context Matters More Than Severity](../knowledge/CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) — `KID-CON-0003`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Risk as canonical concept (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
