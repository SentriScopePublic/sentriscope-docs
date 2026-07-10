---
term: "Identity Privilege"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0031
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0031
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0010
    - KID-GLS-0022
    - KID-GLS-0003
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Identity privilege is the security significance of elevated access an identity holds—admin rights, broad roles, or sensitive scopes—that amplifies blast radius when that identity is compromised or misused."
---

# Identity Privilege

## Definition

**Identity privilege** is the **security significance of elevated access** an [identity](./IDENTITY.md) holds—administrative rights, broad roles, delegated permissions, or sensitive scopes—that **amplifies [blast radius](./BLAST_RADIUS.md)** when that identity is compromised, misused, or investigated as a pivot.

Privilege reflects **what an identity can reach**, not merely its label in a directory. The same credential event on a standard user and a domain administrator is not the same decision.

## SentriScope Usage

SentriScope enriches canonical identities with privilege and access context (`KID-ARC-0001`) so prioritization, attack paths, and investigations can explain **why** identity-related findings rank differently. This entry defines the term only.

## Related terms

- [Identity](./IDENTITY.md) — `KID-GLS-0010`
- [Blast Radius](./BLAST_RADIUS.md) — `KID-GLS-0022`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-009) |
