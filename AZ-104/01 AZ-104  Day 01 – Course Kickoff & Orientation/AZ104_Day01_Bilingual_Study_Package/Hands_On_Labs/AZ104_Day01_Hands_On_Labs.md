# AZ-104 Day 01 — Hands-on Labs (Supplemental)

> These are **recommended practice activities**, not steps performed in the instructor's Day 01 recording. English instructions are followed by Roman Urdu hints. Do not buy hardware or create paid Azure resources just to complete these activities.

## Lab 1 — Requirements discovery for 15 servers
**Objective:** Convert a vague hardware request into an approved requirements document.

**Prerequisites:** Text editor, spreadsheet or Markdown editor.

**Steps:**
1. Invent a fictional client (retail, bank or training company).
2. List services: AD/DNS, web, database, backup, monitoring and management.
3. For every service, estimate owner, expected users, CPU/RAM/storage, availability, RPO/RTO, and dependencies. Mark estimates clearly.
4. Ask whether physical, virtual or cloud deployment is appropriate.
5. Record open questions instead of inventing actual requirements.

**Verification:** You can explain why the answer may be 12, 15 or 18 servers rather than assume 15.

**Troubleshooting:** If a specification is unsupported, mark it *TBD* and ask the application owner.

**Roman Urdu:** Pehle business services aur peak load maloom karein; phir server count justify karein.

## Lab 2 — Rack and power redundancy diagram
**Objective:** Identify failure domains.

**Prerequisites:** Paper, draw.io or Mermaid-capable Markdown editor.

**Steps:** Draw two racks, two independent PDU paths (A/B), dual-PSU hosts, network switches and a management network. Mark what happens when one PDU or switch fails. Identify single points of failure.

**Verification:** At least one planned component failure does not remove every workload; identify limitations honestly.

**Roman Urdu:** Aik PDU fail ho to kaun se servers band honge? Diagram se check karein.

## Lab 3 — CAPEX/OPEX decision worksheet
**Objective:** Compare purchase vs service consumption.

**Steps:** Create input cells for server purchase, networking, support, power, staff, colocation fees, subscriptions and term (12/36 months). Calculate a simple total cost of ownership, keeping capital and operating categories separate.

**Verification:** The total changes correctly when power or number of servers changes. Use hypothetical values only.

**Roman Urdu:** Initial purchase ko monthly costs se alag rakhein; examples ko actual quotes na samjhein.

## Lab 4 — P1 incident simulation
**Objective:** Practice ticket ownership and escalation.

**Scenario:** A customer-facing application becomes unavailable and monitoring shows an affected VM host.

**Steps:** Write an incident ticket with impact, time detected, scope, owner, evidence, first action, escalation contact, communication cadence and restoration validation. Define response and restoration objectives as *fictional contract settings*.

**Verification:** An operator could act from the ticket and would know when to escalate.

**Roman Urdu:** P1 ticket ke liye acknowledgment, impact aur escalation ki clear checklist banayein.

## Lab 5 — Azure portal orientation (low-risk)
**Objective:** Locate management concepts without provisioning anything.

**Steps:** If you already have legitimate Azure access, explore search, subscriptions, resource groups, virtual networks, virtual machines and monitoring pages. Record what each means. **Do not create resources or enter payment details solely for this lab.**

**Verification:** Explain resource vs resource group, subscription and RBAC at a basic level.

**Roman Urdu:** Sirf portal explore karein; paid resources create na karein.
