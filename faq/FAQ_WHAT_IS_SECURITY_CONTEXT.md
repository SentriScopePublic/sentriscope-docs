---
title: "What is security context?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0005
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0003
  explains:
    - KID-GLS-0003
  authority_reference:
    - KID-ARC-0001
website_slug: faq-what-is-security-context
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "Security context is the environmental and relational information—asset role, exposure, identity privilege, business impact, threat relevance—that determines whether a finding actually matters."
---

# What is security context?

## Short answer

**Security context** is the environmental and relational information that determines whether a finding **actually matters**: asset role, exposure, identity privilege, business impact, control coverage, and active threat relevance.

## Explanation

The same vulnerability identifier can be urgent on one asset and irrelevant on another. Context answers *where*, *who*, *what is reachable*, and *what is already exploited in the wild*—not just *what CVE is it*.

Without context, teams sort by generic severity and waste cycles on findings that are technically true but operationally low impact.

## Common mistake

Equating CVSS with organizational risk. CVSS describes a vulnerability in isolation; context describes **your** environment.

## Authority references

- [Security Context](./../glossary/SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Canonical Data Model](./../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001` (entities carrying context)

## Related

- [Understanding Security Context](./../knowledge/UNDERSTANDING_SECURITY_CONTEXT.md) — `KID-CON-0006`
- [Context Matters More Than Severity](./../knowledge/CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) — `KID-CON-0003`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ |
