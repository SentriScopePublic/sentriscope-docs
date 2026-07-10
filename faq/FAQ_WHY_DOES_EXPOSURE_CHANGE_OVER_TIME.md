---
title: "Why does exposure change over time?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0059
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0113
knowledge_relationships:
  depends_on:
    - KID-CON-0113
    - KID-CON-0112
  explains:
    - KID-CON-0113
website_slug: faq-why-does-exposure-change-over-time
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Exposure significance changes as environments, reachability, deployments, and intelligence shift—priority is not fixed at discovery time."
---

# Why does exposure change over time?

## Short answer

Exposure **significance changes** as environments, reachability, deployments, relationships, and intelligence shift—priority is **not fixed** at discovery time.

## Explanation

An exposure discovered last quarter may rank differently today because the asset moved to production, a new integration increased reachability, an attack path became plausible, or threat intelligence raised adversary interest. Conversely, remediation, segmentation, or decommissioning can reduce urgency without changing the CVE score. Teams that treat exposure as a static backlog miss **context drift**—one of the main reasons flat severity lists fail operations.

Guides: [Exposure Context](../knowledge/EXPOSURE_CONTEXT.md) (`KID-CON-0112`) · [Exposure Prioritization](../knowledge/EXPOSURE_PRIORITIZATION.md) (`KID-CON-0113`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-011) |
