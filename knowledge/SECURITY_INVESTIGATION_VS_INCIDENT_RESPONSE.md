---
title: "Security Investigation vs Incident Response"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0005
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0002
  explains:
    - KID-GLS-0002
  related_to:
    - KID-CON-0001
  authority_reference:
    - KID-INV-0001
    - KID-PLT-0002
website_slug: security-investigation-vs-incident-response
last_updated: 2026-07-02
next_review: 2026-07-02
llm_summary: "Investigation seeks validated understanding through evidence; incident response executes containment and recovery under time pressure—they overlap but serve different primary objectives."
knowledge_tags: [investigation, incident-response, education]
---

# Security Investigation vs Incident Response

## What practitioners need to know

Practitioners conflate **investigation** and **incident response** because both occur during crises. They serve different primary objectives.

| | Investigation | Incident Response |
|---|-----------------|-------------------|
| **Primary goal** | Validated understanding | Containment & recovery |
| **Time horizon** | May span weeks | Minutes to hours critical |
| **Output** | Evidence-backed conclusions | Stabilized systems |
| **Success metric** | Correct scope & root cause | Reduced blast radius |

They **overlap** during active incidents—but collapsing investigation into runbook execution loses reasoning quality.

## Industry context

IR playbooks emphasize isolation, eradication, recovery (for example NIST phases). Investigation emphasizes scope, attribution hypotheses, and lessons learned. Skipping investigation after IR produces repeat incidents with undocumented root cause.

## Common mistakes

- Closing IR tickets when systems are up but scope unknown  
- Running IR without preserving evidence for legal/regulatory needs  
- Using investigation tools with no IR handoff (or vice versa)  

## Practical implications

Define **when IR leads** (active exploitation) vs **when investigation leads** (suspicious activity, complex fraud). Preserve evidence packages during IR for post-incident investigation.

Term: [Investigation](../glossary/INVESTIGATION.md) (`KID-GLS-0002`). SentriScope is not a SOAR replacement (`KID-PLT-0002`); investigation support: `KID-INV-0001`.

## Related knowledge

- `KID-CON-0001` — Evidence-Based Investigation  

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial encyclopedia article |
