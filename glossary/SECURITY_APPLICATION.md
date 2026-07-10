---
term: "Security Application"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0033
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0033
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0034
    - KID-GLS-0009
    - KID-GLS-0010
    - KID-GLS-0003
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security application is the software or workload boundary analysts use to reason about business function, data, and risk in security decisions—not a repo, deployment unit, or catalog row alone."
---

# Security Application

## Definition

A **security application** is the **software or workload boundary** analysts use to reason about **business function**, **data**, and **risk** in security decisions.

It is a **decision object**: the capability findings, access events, and exposures attach to when explaining what organizational function could be harmed or abused. It may span multiple technical [services](./SECURITY_SERVICE.md), [assets](./ASSET.md), and [identity](./IDENTITY.md) bindings—not a single repository name or scanner record.

## SentriScope Usage

SentriScope normalizes applications as canonical entities (`KID-ARC-0001`) so prioritization, investigations, and attack paths can explain **why** business impact differs across environments. This entry defines the term only.

## Related terms

- [Security Service](./SECURITY_SERVICE.md) — `KID-GLS-0034`
- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Identity](./IDENTITY.md) — `KID-GLS-0010`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-010) |
