---
title: "What is the difference between an alert and evidence?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0001
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-GLS-0008
  explains:
    - KID-GLS-0001
  authority_reference:
    - KID-INV-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md
website_slug: faq-alert-vs-evidence
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "An alert is a signal that something may need attention; evidence is validated, provenance-bearing information that supports or contradicts a conclusion in an investigation."
---

# What is the difference between an alert and evidence?

## Short answer

An **alert** is a signal that something *may* need attention. **Evidence** is validated, provenance-bearing information that supports or contradicts a specific conclusion during analysis.

Alerts start work; evidence justifies decisions.

## Explanation

Alerts are generated constantly—SIEM rules, scanner findings, EDR detections, threshold breaches. They are optimized for **recall** (notice possibilities), not for **decision quality** alone.

**Evidence** requires context: source, timestamp, linkage to entities, and analyst evaluation. A duplicate alert closed three times is not stronger evidence. A single corroborated log line with asset linkage may be.

| Alert | Evidence |
|-------|----------|
| Machine-generated signal | Evaluated information |
| May be duplicate or noisy | Tracked with provenance |
| Often lacks full context | Supports or contradicts a hypothesis |
| Triage input | Investigation and decision input |

## Common mistake

Treating alert volume as proof of risk severity. Teams measure activity instead of validated exposure and context. See [Finding](./../glossary/FINDING.md) (`KID-GLS-0008`) and [Context Matters More Than Severity](./../knowledge/CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) (`KID-CON-0003`).

## Authority references

- [Evidence](./../glossary/EVIDENCE.md) — `KID-GLS-0001` (term authority)
- [Investigation Workspace](./../investigations/INVESTIGATION_WORKSPACE.md) — `KID-INV-0001` (product capability)

## Related

- [Evidence-Based Investigation](./../knowledge/EVIDENCE_BASED_INVESTIGATION.md) — `KID-CON-0001`
- [From Alerts to Decisions](./../knowledge/FROM_ALERTS_TO_DECISIONS.md) — `KID-CON-0008`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ |
