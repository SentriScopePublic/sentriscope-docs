---
title: "What Is Security Evidence?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0010
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
  explains:
    - KID-GLS-0001
  related_to:
    - KID-CON-0001
    - KID-CON-0002
    - KID-CON-0011
  authority_reference:
    - KID-INV-0001
    - KID-ARC-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-001]
  difficulty: introductory
  audience: [analyst, soc_manager, general]
  estimated_time_minutes: 7
  required_reading:
    - KID-GLS-0001
  recommended_next:
    - KID-CON-0002
    - KID-CON-0011
website_slug: what-is-security-evidence
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Security evidence is verifiable, provenance-bearing information that supports or contradicts an analytical conclusion—not an alert, severity score, or opinion standing alone."
knowledge_tags: [evidence, education, fundamentals]
---

# What Is Security Evidence?

## What practitioners need to know

Practitioners ask: *What counts as evidence in a security investigation?* *Is a SIEM alert evidence?*

**Security evidence** is verifiable information—with known **provenance**—that supports or contradicts a specific conclusion. It is not synonymous with alerts, findings, severity labels, or analyst intuition.

Term authority: [Evidence](../glossary/EVIDENCE.md) (`KID-GLS-0001`).

## What evidence is—and is not

| Is evidence | Is not evidence (alone) |
|-------------|-------------------------|
| Corroborated log lines with source and timestamp | Unvalidated alert text |
| Asset-linked vulnerability with scan metadata | A CVSS score without context |
| Threat intel report with publisher and date | Chat message: "I think it's compromised" |
| Configuration snapshot from authoritative CMDB | Duplicate closed ticket |

Evidence may **support** or **contradict** a hypothesis. Both roles matter.

## Industry context

Incident response frameworks, audit standards, and legal discovery all assume teams can produce **what they knew and how they knew it**. Organizations that conflate alert volume with evidence quality struggle in post-incident review and regulatory inquiry.

Digital forensics distinguishes **data** from **evidence** through chain-of-custody and validation. Security operations increasingly adopt the same discipline for everyday investigations—not only forensic cases.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Calling every alert "evidence" | Inflated confidence; poor prioritization |
| Discarding contradictory data | Confirmation bias |
| Exporting data without source metadata | Non-reproducible conclusions |
| Treating age as irrelevant | Decisions on stale state |

## Practical implications

1. **Label the source** — system, collection time, collection method.  
2. **Link to entities** — asset, identity, application where possible.  
3. **State the claim** — what conclusion does this item support or refute?  
4. **Separate signal from proof** — alerts initiate work; evidence justifies outcomes.  

See [From Alerts to Evidence](./FROM_ALERTS_TO_EVIDENCE.md) (`KID-CON-0017`) and [Evidence-Based Investigation](./EVIDENCE_BASED_INVESTIGATION.md) (`KID-CON-0001`).

## Limitations

Evidence quality varies. Low-quality evidence may still warrant exploration—it should not silently drive irreversible action without corroboration. No single field (severity, confidence, age) replaces multidimensional evaluation. See `KID-CON-0002`.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0001 | [Evidence](../glossary/EVIDENCE.md) |
| KID-GLS-0008 | [Finding](../glossary/FINDING.md) |
| KID-CON-0002 | [What Makes Security Evidence Trustworthy](./WHAT_MAKES_SECURITY_EVIDENCE_TRUSTWORTHY.md) |
| KID-FAQ-0001 | [Alert vs evidence](../faq/FAQ_ALERT_VS_EVIDENCE.md) |
| KID-FAQ-0009 | [What is evidence in investigation?](../faq/FAQ_WHAT_IS_EVIDENCE_IN_INVESTIGATION.md) |

## Authority references

- `KID-INV-0001` — [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md)
- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
