---
title: "What is the difference between correlation and aggregation?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0062
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0122
knowledge_relationships:
  depends_on:
    - KID-CON-0122
  explains:
    - KID-CON-0122
    - KID-GLS-0013
website_slug: faq-correlation-vs-aggregation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Aggregation counts or groups observations; correlation links them into entity-aware stories that may change rank, scope, or communication."
---

# What is the difference between correlation and aggregation?

## Short answer

**Aggregation** combines observations by rule—counts, rollups, time windows, deduplication. **Correlation** links observations because they inform the **same security understanding**—often across entity types and sources—and may **change the decision**.

## Explanation

A SIEM that groups fifty login failures into one alert is aggregating. An analyst who links those failures to a privilege change on a crown-jewel path is correlating—and may escalate differently than either signal alone would justify.

If linkage only reduces noise without changing rank, scope, or narrative, it is aggregation—not correlation in the decision-support sense.

Guide: [Correlation vs Aggregation](../knowledge/CORRELATION_VS_AGGREGATION.md) (`KID-CON-0122`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-012) |
