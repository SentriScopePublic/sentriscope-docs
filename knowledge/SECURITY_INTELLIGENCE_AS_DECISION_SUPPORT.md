---
title: "Security Intelligence as Decision Support"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0077
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0070
    - KID-CON-0073
    - KID-GLS-0023
    - KID-CON-0049
  synthesizes:
    - KID-CON-0070
    - KID-CON-0071
    - KID-CON-0072
    - KID-CON-0073
    - KID-CON-0074
    - KID-CON-0075
    - KID-CON-0076
    - KID-CON-0058
    - KID-CON-0068
  related_to:
    - KID-GLS-0028
  authority_reference:
    - KID-TIN-0001
    - KID-OIN-0001
navigation:
  knowledge_series: SER-007
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0076
  recommended_next:
    - KID-CON-0080
website_slug: security-intelligence-as-decision-support
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Volume 2 synthesis: organizations integrate external threat intelligence and internal operational intelligence with Volume 1 evidence, investigation, risk, and attack paths to produce explainable security decisions."
knowledge_tags: [security-intelligence, decision-support, education]
---

# Security Intelligence as Decision Support

## What practitioners need to know

This article closes **SER-007** and **Volume 2 — Intelligence** with the **core thesis**: organizations integrate external and internal intelligence into a **unified security decision process**—not into parallel silos, feed subscriptions, or autonomous tooling.

## The Volume 2 decision-support model

```text
Volume 1 foundations:
  Evidence + Investigation + Risk + Attack Paths
                        ↓
Volume 2 intelligence:
  Threat Intelligence (external) + Operational Intelligence (internal)
                        ↓
Security Intelligence (integrated reconciliation)
                        ↓
              Prioritized, explainable action
```

Term: [Decision Support](../glossary/DECISION_SUPPORT.md) (`KID-GLS-0023`).  
Term: [Security Intelligence](../glossary/SECURITY_INTELLIGENCE.md) (`KID-GLS-0028`).

## Curriculum convergence

| Volume / Series | Contribution |
|-----------------|--------------|
| VOL-001 SER-001 | Trustworthy evidence |
| VOL-001 SER-002 | Investigation discipline |
| VOL-001 SER-003 | Risk prioritization |
| VOL-001 SER-004 | Attack path context |
| VOL-002 SER-005 | External knowledge → decisions |
| VOL-002 SER-006 | Internal knowledge → decisions |
| **VOL-002 SER-007** | **Integrated intelligence → decisions** |

## Operating principles

| Principle | Meaning |
|-----------|---------|
| **Integration is process** | Not a product label (`KID-CON-0071`) |
| **Evidence leads conclusions** | Intelligence adapts on conflict (`KID-CON-0076`) |
| **Risk context anchors business judgment** | Intelligence enriches, not replaces (`KID-CON-0031`) |
| **Explainability is mandatory** | Reason codes for TI, OI, risk, evidence |
| **Confidence is communicated** | `KID-GLS-0024`, `KID-CON-0075` |
| **Misconceptions are corrected early** | `KID-CON-0072` |
| **Intelligence has limits** | `KID-CON-0057`, `KID-CON-0067` |

## Operating checklist

Before acting on integrated intelligence:

1. ☐ Are TI relevance and OI urgency reconciled—or is conflict documented?  
2. ☐ Does evidence support, contradict, or remain insufficient?  
3. ☐ Is risk context and residual risk stated?  
4. ☐ Are attack paths considered for structural exposure?  
5. ☐ Can another analyst audit the rationale?  
6. ☐ Is stakeholder communication proportional to confidence?  

## Practical implications

- **Embed** integration rules in triage, patch, hunt, and escalation runbooks.  
- **Train** with SER-007 misconceptions article before tool changes.  
- **Prepare** for Volume 3 — the security entities intelligence and investigation operate on.  

## Limitations

Decision support quality depends on inventory accuracy, source curation, governance, and analyst skill—integration architecture alone does not operationalize intelligence.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0028 | [Security Intelligence](../glossary/SECURITY_INTELLIGENCE.md) |
| KID-CON-0072 | [Common Misconceptions About Security Intelligence](./COMMON_MISCONCEPTIONS_ABOUT_SECURITY_INTELLIGENCE.md) |
| KID-FAQ-0040 | [What is security intelligence decision support?](../faq/FAQ_WHAT_IS_SECURITY_INTELLIGENCE_DECISION_SUPPORT.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)
- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 synthesis; Volume 2 intelligence capstone |
