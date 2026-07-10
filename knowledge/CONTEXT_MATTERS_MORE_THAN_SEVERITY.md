---
title: "Context Matters More Than Severity"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0003
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0003
    - KID-GLS-0004
    - KID-GLS-0007
  explains:
    - KID-GLS-0003
  related_to:
    - KID-CON-0004
    - KID-CON-0009
  authority_reference:
    - KID-ARC-0001
    - KID-OIN-0001
website_slug: context-matters-more-than-severity
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "Practitioners should prioritize findings by security context—exposure, asset role, identity privilege, and threat relevance—not generic severity scores alone such as CVSS in isolation."
knowledge_tags: [context, risk, prioritization, education]
---

# Context Matters More Than Severity

## What practitioners need to know

Practitioners ask: *How do I prioritize vulnerabilities?* *Why are CVSS scores insufficient?*

**Severity** describes a finding in isolation. **Context** describes whether it matters **in your environment**. Mature programs prioritize by context-enriched **risk**, not raw score sorting.

## Industry context

CVSS, scanner ratings, and EPSS provide useful **inputs**. They do not encode:

- Internet exposure vs isolated segment  
- Privileged identity pathways  
- Active exploitation in the wild (threat relevance)  
- Missing compensating controls  
- Business criticality of the affected application  

Two identical CVE records can warrant opposite urgency.

## Common mistakes

| Mistake | Result |
|---------|--------|
| "Fix all Critical first" | Neglected reachable medium issues |
| Ignoring asset role | Patches on lab while prod identity exposed |
| No threat enrichment | Miss known-exploited prioritization |
| Duplicate counting | Same issue across five tools = false urgency |

## Practical implications

1. Normalize findings to **entities** (assets, identities).  
2. Enrich with **reachability** and **threat** context.  
3. Rank by explainable **risk**, document why.  
4. Revisit when context changes (new exposure, new campaign).  

Glossary: [Security Context](../glossary/SECURITY_CONTEXT.md) (`KID-GLS-0003`), [Risk](../glossary/RISK.md) (`KID-GLS-0004`), [Exposure](../glossary/EXPOSURE.md) (`KID-GLS-0007`).

## Related knowledge

- `KID-CON-0009` — Why Correlation Matters  
- `KID-FAQ-0005` — What is security context?  

## Authority references

- `KID-ARC-0001` — canonical entities carrying context  
- `KID-OIN-0001` — operational prioritization surfaces  

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial encyclopedia article |
