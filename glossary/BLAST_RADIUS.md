---
term: "Blast Radius"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0022
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0022
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0011
    - KID-GLS-0003
  explains:
    - KID-CON-0046
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Blast radius is the scope of potential impact if a compromise succeeds—systems, users, data, or services affected downstream of an entry point or path step."
---

# Blast Radius

## Definition

**Blast radius** is the **scope of potential impact** if a compromise succeeds at a given point—how many **systems**, **users**, **data sets**, or **services** could be affected downstream.

In attack path analysis, blast radius helps translate structural reachability into **business-meaningful** prioritization.

## Usage in attack path decisions

| Question | Blast radius role |
|----------|-------------------|
| Why prioritize this hop? | Large downstream impact |
| Executive briefing | Impact in business terms |
| Control investment | Reduce radius at choke points |

## Related terms

- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Related knowledge

- [Attack Paths and Business Impact](../knowledge/ATTACK_PATHS_AND_BUSINESS_IMPACT.md) — `KID-CON-0046`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-004) |
