---
term: "Unknown Identity"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0032
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0032
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0010
    - KID-GLS-0003
    - KID-GLS-0030
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "An unknown identity exists in activity or directory sources but lacks sufficient context for confident security decisions—uncertainty about role, ownership, or privilege, not merely an unmapped account name."
---

# Unknown Identity

## Definition

An **unknown identity** is an [identity](./IDENTITY.md) that **exists in activity or directory sources** but **lacks sufficient context** for confident security decisions.

The uncertainty is about **role, ownership, privilege, and relationships**—who the identity represents, what it can access, and whether it is expected—not merely an unmapped username or service principal label. Authentication or log activity may surface the entity; decision support still requires context enrichment.

## Related terms

- [Identity](./IDENTITY.md) — `KID-GLS-0010`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Unknown Asset](./UNKNOWN_ASSET.md) — `KID-GLS-0030`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-009) |
