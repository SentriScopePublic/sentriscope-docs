---
title: "Does security evidence expire?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0006
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0012
  - KID-GLS-0001
  - KID-CON-0015
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-CON-0012
  explains:
    - KID-CON-0012
  authority_reference:
    - KID-INV-0001
website_slug: faq-does-evidence-expire
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Evidence does not have a universal expiry date—freshness depends on evidence type and the decision being made; stale evidence requires explicit caveats or re-validation."
---

# Does security evidence expire?

## Short answer

Evidence does not have a single universal expiry date. **Freshness** depends on evidence type and the decision at hand—what is adequate for quarterly planning may be unacceptable during active incident containment.

## Explanation

[Evidence freshness](../knowledge/EVIDENCE_FRESHNESS.md) (`KID-CON-0012`) is contextual:

- Live EDR status may be stale within minutes during an attack.  
- A vulnerability scan may remain useful for days until patch deployment.  
- Architecture documentation may support classification for months.  

Retention policies (legal, regulatory) also govern how long evidence must be **kept**—distinct from whether it is **fresh enough to use**.

## Common mistake

Assuming "we looked at this last week" means the environment is unchanged. Re-validate before irreversible actions.

## Related

- [Evidence Lifecycle](../knowledge/EVIDENCE_LIFECYCLE.md) — `KID-CON-0015`
- [Evidence](../glossary/EVIDENCE.md) — `KID-GLS-0001`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ — SER-001 |
