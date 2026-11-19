# AZ-104 — Day 01 | Detailed English Class Notes

> **Source:** `AZ-104-day-01.txt` (the supplied classroom transcript). This is a detailed, topic-wise rendering of the lecture, **not a verbatim sentence-by-sentence translation**. The unchanged original is included in the package. Speaker identification in the automatic transcript is unreliable; exchanges are presented by role rather than invented attributions.

## 1. Opening: introductions and learning goals

The instructor opens the session by asking each participant to introduce themselves and explain why they enrolled in the cloud-computing course. One participant explains that they are transitioning into IT from a non-IT profession, have studied Linux, passed the RHCSA examination, and want to build cloud skills for an IT job. The instructor also asks about their location and professional background. Another participant describes experience spanning oil and gas, Linux/Unix, DevOps/SRE concepts, observability, and banking-industry work. The class establishes that attendees have different technical backgrounds and that foundational concepts should not be assumed.

The instructor introduces the slogan **“Learn, Earn, and Grow.”** He describes a career spanning Windows Server, Exchange, VMware virtualization, Azure, corporate training, data-center architecture, and solution design. He discusses AS Network Zone and System SLA Technologies and encourages the class to use course recordings and learning resources. These are the instructor’s accounts of professional experience, not independently verified credentials.

**Classroom lesson:** A good administrator asks questions, identifies skill gaps, and connects what is taught to actual job responsibilities.

## 2. AZ-104 training scope and certification pathway

The instructor presents the course as a practical administration track beginning with cloud fundamentals and progressing toward complex infrastructure operations. He contrasts **AZ-900** as an introductory Azure-fundamentals exam with **AZ-104** for Azure administrator skills, and mentions **AZ-305** as a later architecture-oriented pathway. At one point the transcript renders “AZ-400”; the surrounding discussion focuses on AZ-104, so this appears to be a transcription or speaking slip. The instructor discusses an approximately six-week class format with shorter daily sessions as opposed to a compact full-day schedule.

He repeatedly asks students to **think like infrastructure administrators or data-center architects**, not merely operators following button-click instructions. This includes understanding the business requirement before selecting computing, storage, or network solutions.

### Course domains introduced

- **Identity and governance:** cloud identities, access control, subscriptions and organizational restrictions.
- **Storage:** storage services, capacities, deployment and management.
- **Compute:** Windows and Linux virtual machines, server management, and workloads.
- **Networking:** IP addressing, subnetting, CIDR/VLSM, routing, switching, virtual networks, and firewalls.
- **Monitoring and operations:** resource consumption, CPU, memory, storage, service health, and cost.

The instructor introduces **Azure Virtual Desktop (AVD)** as an example of user computing hosted centrally. He compares the general concept with VMware Horizon and other VDI solutions. He emphasizes that managing virtual desktops is related to, but is not the same as, general server administration.

## 3. Career-level context: L1, L2, L3 and architecture

The instructor uses L1/L2/L3/L4-style labels to illustrate increasing support responsibilities, from basic operations to advanced troubleshooting and architecture. These are organizational job-level conventions; there is no universal mapping from an Azure certification to an L-level job title. Students are encouraged to learn the actual technologies and production workflows rather than assume a certification automatically provides a particular support level.

## 4. Foundational idea: traditional IT → virtualization → cloud

The instructor introduces three successive approaches to running infrastructure:

1. **Traditional IT:** procure physical equipment, arrange rack space, power, cooling, connectivity, security and operating staff, then install the operating systems and services.
2. **Virtualization:** use a hypervisor so multiple workloads can run on fewer physical hosts, improving utilization and flexibility.
3. **Cloud computing:** consume provider-managed infrastructure and services using defined service models and billing arrangements.

He uses an everyday analogy—moving from a bicycle to a motorcycle and then a car—to discuss how requirements, capabilities, and costs change. His point is that administrator responsibilities persist even when the implementation platform changes.

## 5. The 15-server customer role-play: setting the scene

The class conducts a long role-play: imagine the students and instructor work for a **shared/colocation data-center provider**, using Sify as a classroom example. A customer wants **15 new physical servers** installed. The instructor alternates between customer and provider perspectives to teach requirement gathering.

At first, students mention processor, RAM, disk, network, applications, connectivity, and 24-hour support. The instructor acknowledges these but asks the class to go much deeper. A request for “15 servers” is not enough information to begin a responsible build.

### Ask the customer

- **What services or business workloads** will run? Examples discussed include domain controllers, DNS, DHCP, databases, web services, file servers, and print servers.
- **Why exactly 15 servers?** Is this a calculated capacity requirement, or merely an estimate? Could fewer or more be needed?
- What are the CPU, memory, storage, network throughput and growth requirements of each workload?
- Who **owns and purchases** the physical machines: the client, or the colocation/service provider?
- Does the client need **remote management** access, and what security controls will govern it?
- What contractual availability, maintenance, support, and response expectations apply?

The instructor highlights professional phrasing: ask about the **services delivered by servers**, not just whether software can be installed. A meaningful design begins with business capabilities and workloads, then derives hardware requirements.

## 6. Ask the data-center provider

From the customer's side of the table, the class explores the due-diligence checklist:

### Geographic location and site hazards

Where will the servers be physically housed? What happens if a flood, earthquake, regional outage, travel restriction, or other disruption prevents engineers entering the site? Are there diverse locations or disaster-recovery arrangements?

### Cooling and environment

Is the facility designed for reliable temperature, humidity, airflow, and environmental monitoring? Would the equipment suffer from a cooling failure? The instructor draws an analogy with joining an English-speaking learning environment: the setting matters to the outcome. **No particular extreme temperature in the recording should be treated as a recommended standard.**

### Power redundancy

What utility feeds, UPS/generators, rack power distribution units (PDUs), and redundant supply options exist? If a PDU fails, is equipment still powered? Can dual power supplies be fed from separate power paths?

### Rack diversity and common failures

The instructor asks whether placing all 15 machines in one rack makes sense. A rack-level issue (for example, power distribution failure) could affect the entire workload. Splitting infrastructure across racks or power domains can improve resilience, subject to budget and topology.

### Physical access and security

Customers may own servers without automatically receiving unrestricted access to the shared facility. The instructor discusses controlled visits, escorted access, other customers' equipment, security rules, cleanliness and restrictions on touching shared network infrastructure. Actual entry policies are provider-specific.

### Remote administration

Will the facility offer remote-hands assistance and out-of-band management, so approved administrators can operate servers without routine physical visits?

## 7. Private vs shared/public data centers

The instructor contrasts a company-operated **private data center** (an organization controls its equipment and uses it for its own operations) with a **shared provider facility** accommodating multiple customers under different ownership and contractual models. System SLA Technologies and AS Network Zone are used as illustrative organizations. A shared facility can lease space, power, cross-connects and optional managed equipment; the precise arrangement varies by agreement.

**Important distinction:** A commercial colocation facility is not automatically the same thing as a **public cloud**. Their tenancy, abstraction, self-service, elasticity, and operating responsibilities differ.

## 8. CAPEX and OPEX

The instructor introduces **CAPEX (capital expenditure)** for substantial up-front investments in infrastructure and **OPEX (operating expenditure)** for recurring operating costs such as staffing, power, ongoing maintenance, and service subscriptions. The exact accounting classification depends on the nature of expenditure; purchasing additional servers may still be capital expenditure even after the data center is running.

The class is asked to see why a small organization cannot simply budget for 15 boxes. Facilities, support, networking, licenses, redundancy, and long-term operations must also be considered.

## 9. SLA, priority and operational response

The final portion of this supplied transcript introduces **SLA — Service Level Agreement**. A customer asks: if one of the 15 servers becomes unavailable, when will the provider acknowledge and restore service?

The instructor describes **P1–P5** as **priority** categories, explaining that priorities differ by business impact and urgency. A bulk request to create around 1,200 new accounts is used as an example of work that can be scheduled rather than treated as an immediate production outage. The lecture gives illustrative response windows such as approximately 5–10 minutes for P1 and longer windows for lower priorities; those numbers are **examples, not a universal industry SLA**.

Two separate measures are introduced:

- **Response SLA:** time to acknowledge, own, or begin action on the ticket.
- **Resolution/restoration SLA:** contractual target for fixing the issue or restoring the affected service.

For high-priority tickets, the instructor describes contacting the assigned engineer directly as well as assigning the ticket. The example of a server approaching very high CPU use emphasizes prompt triage, business impact, and handoff.

**Transcript boundary:** The supplied recording ends while the instructor is still explaining the P1 resolution scenario. Do not invent the rest of the lecture.

## 10. Classroom discussion and analogies worth remembering

- **Career change and learning:** participants have diverse backgrounds and can build skills with structured study.
- **15-server exercise:** learn to switch between customer and provider perspectives.
- **Speaking professionally:** translate vague infrastructure requests into services, measurable capacity, and contractual requirements.
- **Environment analogy:** a well-designed facility supports reliability, just as the right learning environment supports progress.
- **Bicycle-to-car analogy:** growing capability changes costs and operational requirements.
- **P1 phone call:** incident ownership includes communication, not merely clicking “assign.”

## 11. Revision checklist

You should be able to explain the five broad AZ-104 administration areas, compare traditional IT/virtualization/cloud, articulate a 15-server requirements interview, explain site redundancy, distinguish colocation from public cloud, define CAPEX/OPEX, and distinguish SLA response from resolution targets.

> For checked technical clarifications and supplemental study material, see `Technical_Verification/` and `Hands_On_Labs/`. Those files are **not instructor quotations**.
