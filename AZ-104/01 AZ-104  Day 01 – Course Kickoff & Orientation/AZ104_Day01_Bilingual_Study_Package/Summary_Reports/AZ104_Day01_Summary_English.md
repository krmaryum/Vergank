# AZ-104 Day 01 — Summary Report (English)

## Overview
The instructor establishes the Azure administrator learning roadmap and uses an extended 15-server data-center case study to teach infrastructure thinking, customer discovery, facility resilience, costs, and SLAs.

## Learning objectives
- Understand the AZ-900 → AZ-104 → AZ-305 learning pathway as presented in class.
- Identify broad identity, storage, compute, networking and monitoring responsibilities.
- Compare traditional physical infrastructure, virtualization and cloud.
- Build a structured requirements checklist for a 15-server request.
- Distinguish CAPEX, OPEX, response SLAs and restoration SLAs.

## Topics covered
Introductions; instructor background; L1–L3 discussion; course roadmap; Azure Virtual Desktop overview; fundamental networking; traditional IT; data-center role-play; private versus shared facilities; rack, cooling, power and remote access; service priority P1–P5.

## Core concepts
A server request is a business-service request. Hardware sizing follows workload requirements. Availability requires failure-domain planning (power, rack, site, and people). Cost comprises purchase plus ongoing operations. Incident priority and contractual SLA must be agreed rather than assumed.

## Classroom scenario
A customer asks a Sify-style shared facility to install 15 physical servers. Students initially ask about CPU, memory, storage and networking. The instructor expands the discussion to location hazards, cooling, dual power, rack-level failures, facility access, remote management, ownership, workload sizing and service agreements.

## Key takeaways
1. Think as a customer **and** as an administrator.
2. Ask why 15 servers are needed before proposing hardware.
3. Design for service reliability rather than only equipment counts.
4. Separate initial capital costs from recurring service costs.
5. Response time and restoration time are different measures.

## Interview questions to rehearse
Why does a company use colocation? How would you validate a 15-server requirement? What is a rack/PDU failure domain? What is CAPEX versus OPEX? How do P1 and P5 differ? What does an Azure Administrator manage?

## Suggested hands-on labs (extra; not demonstrated in lecture)
Create an infrastructure requirements worksheet; draw a redundant rack/power topology; model purchase versus operating costs; write a P1 incident acknowledgment and escalation procedure; explore Azure Portal navigation without creating paid resources.

## Scope note
The recording ends mid-discussion of P1 resolution targets. This report does not assume the instructor completed that topic.
