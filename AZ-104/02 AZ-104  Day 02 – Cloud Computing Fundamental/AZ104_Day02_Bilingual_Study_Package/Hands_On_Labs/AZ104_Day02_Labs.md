# AZ-104 Day 02 — Suggested Hands-on Labs

> **Additional suggestions, not activities performed in the uploaded lecture.** Run with an Azure subscription only after confirming its current billing and free-trial terms. Do not publish services unnecessarily.

## Lab 1 — Cost-model worksheet
**Objective:** Compare illustrative CAPEX and OPEX against a cloud monthly-spend model.
**Prerequisites:** Spreadsheet or Markdown editor.
**Steps:** 1. Record instructor example figures: ₹1 crore initial and ₹20 lakh per month. 2. Separate capital and recurring items. 3. Create a hypothetical Azure operating budget with no invented provider prices. 4. Record missing inputs needed for a fair comparison.
**Verification:** All assumptions labeled and no class estimate presented as a quote.
**Troubleshooting:** Check units (lakh, crore, month, year) and include data-transfer/support/licensing costs.

## Lab 2 — Design the diamond-business architecture
**Objective:** Identify core DNS, DHCP, AD DS, website/application, backup and monitoring responsibilities.
**Prerequisites:** Diagramming tool or text editor.
**Steps:** Draw users, branch/office, primary data center, DR site and internet; mark critical services, redundancy and trust boundaries.
**Verification:** Diagram shows primary/DR separation, network connectivity and system dependencies.
**Troubleshooting:** Avoid interpreting one classroom server per service as a universal best practice.

## Lab 3 — Compare cloud deployment patterns
**Objective:** Distinguish public, private, hybrid and multi-cloud.
**Steps:** Classify (a) Azure-only hosting, (b) one organization dedicated on-premises cloud, (c) on-prem + Azure integration, (d) Azure + AWS without on-prem.
**Verification:** Answers: public, private, hybrid, multi-cloud respectively.

## Lab 4 — RTO/RPO planning exercise
**Objective:** Create distinct recovery and data-loss objectives.
**Steps:** For a critical order system, pick hypothetical RTO of 2 hours and RPO of 15 minutes. Write down recovery priorities, backup cadence, replication and restore test evidence.
**Verification:** RTO is not confused with RPO; values explicitly described as examples.

## Lab 5 — Azure account safety checklist
**Objective:** Prepare for instructor-led portal exercises.
**Steps:** Review current official free-account eligibility and payment terms; decide on account timing; enable MFA; create budget and alerts; list expected resource costs and cleanup steps.
**Verification:** MFA enabled, budget created, resource naming and cleanup plan recorded.
**Troubleshooting:** If free account unavailable, do not incur charges without knowing billing terms.

## Lab 6 — Region-selection decision table
**Objective:** Pick a hypothetical Azure region based on constraints.
**Steps:** Compare geographic proximity, services, pricing, data-residency needs and resilience design using current official Azure documentation.
**Verification:** Recommendation includes tradeoffs; region and zone are not treated as identical concepts.

## Lab evidence to capture
- Architecture diagram
- Cost model and assumptions
- RTO/RPO worksheet
- Azure budget alert configuration (without showing payment data)
- Region comparison notes
- Lab cleanup checklist
