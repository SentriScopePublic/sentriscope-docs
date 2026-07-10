---
title: "What is a security asset?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0041
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0080
knowledge_relationships:
  depends_on:
    - KID-CON-0080
  explains:
    - KID-CON-0080
website_slug: faq-what-is-a-security-asset
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security asset is a resource relevant to protection and investigation—servers, endpoints, cloud workloads, and similar—enriched with context that changes how findings are interpreted."
---

# What is a security asset?

## Short answer

A **security asset** is a **resource** in your environment—servers, endpoints, cloud workloads, databases, and similar—that **anchors findings, exposures, and investigations**. It is a **decision lens**, not just an inventory row.

## Explanation

Assets matter because security work attaches to **things that can be affected**: a CVE on a lab VM is not the same decision as the same CVE on a production payment service. Context—ownership, environment, dependencies, and [asset criticality](../glossary/ASSET_CRITICALITY.md) (`KID-GLS-0029`)—changes what analysts prioritize and how they explain risk.

Guide: [Understanding Security Assets](../knowledge/UNDERSTANDING_SECURITY_ASSETS.md) (`KID-CON-0080`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-008) |
