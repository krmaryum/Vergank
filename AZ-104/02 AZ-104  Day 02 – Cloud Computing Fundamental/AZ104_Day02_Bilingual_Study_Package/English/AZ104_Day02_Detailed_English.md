# AZ-104 — Day 02 | Detailed English Class Notes

> **Type:** Topic-organized detailed notes based on the uploaded classroom transcript. These are NOT a complete line-by-line translation. The unchanged 704-line transcript is included in the ZIP for full fidelity. Technical corrections are in a separate file.

## Source coverage

Full transcript reviewed: lines 1–704. Notes follow the original lecture order and preserve the major teaching examples, questions, scenarios and discussions.

## 01. Role of an Infrastructure Administrator

**Transcript reference:** Lines 1–9

The instructor begins by revisiting Day 01 and emphasizes that the course should be approached from the perspective of a company's infrastructure administrator rather than from one narrow job title. An administrator may receive responsibilities for virtual machines, physical servers, networking, storage, operating systems, application services, and troubleshooting. Understanding how these dependencies fit together is the real goal of studying cloud computing. The lesson is therefore not simply a sequence of Azure portal screens; it is the business and operations context behind those screens. The instructor also links this lesson to previous discussions about data centers and ticketing tools.

## 02. On-Premises and Why Organizations Need Servers

**Transcript reference:** Lines 10–42

Nadeem describes on-premises infrastructure as physical or bare-metal servers installed and managed in the organization's premises, including racks and networking. The instructor connects server infrastructure to concrete services: DHCP assigns network configuration automatically, DNS provides name resolution, Active Directory Domain Services centralizes identities, and web servers publish sites and applications. He contrasts traditional office desktops with laptops that enable remote work and explains why manually assigning IP addresses on hundreds of devices does not scale well. He says an organization will normally deploy multiple servers for critical services so that one server's failure does not automatically stop service. The lecture is meant as a cloud introduction: individual Windows Server roles are not being taught in full depth here.

## 03. The Diamond-Business Data Center Scenario

**Transcript reference:** Lines 43–52

The teacher asks learners to imagine that Nadeem and Khalid own a new diamond business serving the UAE and hire him as the first infrastructure administrator. He must recommend and deploy the IT foundation for the company's users, website, and applications. His first request is an appropriate data center room or facility. Important planning areas include cooling, reliable and redundant electricity, a UPS or generators, sufficient physical servers and spare capacity for growth, switches, routers, firewalls, load balancers, licensing, and the staff who will maintain the environment. He illustrates redundancy by planning additional servers beyond the immediately required amount. He also explains that having seven services can imply more than seven deployed server instances when resilience and secondary systems are considered. The exact cooling temperature and server counts mentioned are classroom examples, not universal requirements.

## 04. CAPEX and OPEX for Traditional IT

**Transcript reference:** Lines 52–80

The instructor uses illustrative Indian-rupee figures for the diamond-company data center: a physical server is estimated at around ₹10 lakh, a sample networking set at ₹8 lakh, and an initial implementation budget at roughly ₹1 crore. This up-front investment is introduced as CAPEX (capital expenditure). Recurring costs—administrator salaries, power, cooling, repairs, maintenance, software licensing and other operating charges—are explained as OPEX (operating expenditure). A hypothetical ₹20 lakh per month is used for operating expense. The figures are not an actual vendor quotation or a universal Azure-vs-on-premises total-cost comparison; their role is to make the ownership model understandable.

## 05. Disaster Recovery, RTO, and RPO

**Transcript reference:** Lines 81–145

A natural disaster, restricted access to a building, or a major facility failure may make the primary data center unavailable. The instructor therefore introduces a geographically separate disaster-recovery (DR) site, using Delhi and Bengaluru as an example. Critical applications and systems may need a recovery copy, but full duplication also raises infrastructure costs. The discussion introduces RTO (Recovery Time Objective) and RPO (Recovery Point Objective), replication lag, and the possibility of lost recent changes. The instructor's one-hour example illustrates that recovery data may be older than the last production update. A technical clarification is important: RTO describes how long recovery may take, while RPO describes how much data loss measured in time is acceptable; they are not interchangeable. Traditional on-premises data centers and DR locations still exist even after cloud adoption.

## 06. Limits of Physical-Server Expansion

**Transcript reference:** Lines 146–160

In a traditional hardware deployment, an application may outgrow its original allocation—for example, a server with 16 GB RAM and four CPU cores may require more memory and compute. The lecture describes a conventional workflow in which the machine is shut down, hardware is upgraded and service restarted. That interruption can affect business operations. The point is to motivate flexibility and efficiency: organizations must not assume that their initial sizing will remain sufficient forever. Some hardware configurations allow more flexible changes, but the classroom contrast is between a manually modified physical server and more agile virtualized provisioning.

## 07. Virtualization: Consolidation, Efficiency and Hypervisors

**Transcript reference:** Lines 160–211

Virtualization is presented as an important bridge between traditional IT and cloud computing. The teacher highlights server consolidation: several workloads can run as virtual machines on fewer physical hosts, reducing floor space, power, cooling and sometimes total CAPEX and OPEX. He relates this to a “Go Green” motivation. He discusses Type 1 and Type 2 hypervisors, VMware Workstation, VMware's continued role in the market after Broadcom, Nutanix, and integrations with public clouds. The instructor gives an example of replacing fourteen physical deployments with a smaller host estate; real capacity depends on CPU, RAM, storage IOPS, resilience and workload sizing. Hot-add of vCPU or memory is not guaranteed merely because a hypervisor is Type 1; it depends on the platform, virtual-machine configuration and guest OS. The lecture's history of RAID and virtualization is best treated as an instructor anecdote pending verification.

## 08. Why Cloud Computing and the Airline Analogy

**Transcript reference:** Lines 211–234

The lesson introduces AWS, Microsoft Azure and Google Cloud Platform as major providers. Its central teaching analogy compares buying an entire aircraft for one journey with buying a seat on an existing flight. The first resembles owning the complete data center; the second resembles consuming a provider's shared infrastructure without purchasing its physical servers. This leads to pay-as-you-go consumption, elastic capacity and shorter time to deploy business applications. The provider still operates physical infrastructure and data centers: the cloud is not a place without hardware. The instructor makes historical claims about NIST and the dates when providers developed cloud offerings and exams; those claims are retained as lecture content, not presented as independently verified history.

## 09. Public, Private, Hybrid and Multi-Cloud Choices

**Transcript reference:** Lines 235–326

The instructor explores where workloads should live. Public cloud provides resources to many customers on a shared provider platform; private cloud is dedicated to one organization; hybrid cloud combines an on-premises or private environment with a public-cloud environment. The lecture also mentions placing resources with Microsoft and AWS to improve resilience; using more than one public-cloud provider is more precisely called multi-cloud and is not, by itself, the definition of hybrid cloud. Learners ask whether a shared public-cloud server must be virtual or physical. The important distinction is that public clouds use real physical hardware while providing logically isolated customer services. The class discusses risks from a provider outage and strategies to spread critical workloads, though distributing work across providers introduces complexity and cost.

## 10. Cloud Benefits, Security, Data Control and Risk

**Transcript reference:** Lines 327–448

The teacher lists fast provisioning, scalability (vertical and horizontal), potential high availability, easier access to public addressing, update or automation options, backup and disaster-recovery products, and faster time to market. He also emphasizes practical concerns: outages, operational dependency on external providers, the location and handling of sensitive data, compromised identities and unauthorized access. The class discusses whether particular data should stay on-premises and recommends a mixed deployment when business risk warrants it. Technical distinction: cloud providers offer security controls, but customers remain responsible for configuring identity, permissions, networks, data protection and other controls appropriate to the service model. A powered-off virtual machine can still incur storage and network-related charges; shutting down services does not necessarily make a bill zero.

## 11. Cloud Architecture and Service Models

**Transcript reference:** Lines 449–482

The class moves from cloud deployment types to the front end and back end of a cloud system and then to service models. In on-premises IT, the customer manages hardware, storage, networking, virtualization, OS, middleware, runtime, applications and data. With IaaS, the provider typically manages the physical infrastructure and virtualization while the customer retains responsibility for guest OS, applications, identities and data. PaaS shifts more platform and runtime responsibility to the provider so developers focus more on their application and data. SaaS delivers ready-to-use applications, with configuration, access governance and data responsibilities still relevant to the customer. The original lesson explains these as layers of responsibility rather than as a cloud portal checklist.

## 12. Azure Provider Comparison and Account Overview

**Transcript reference:** Lines 483–574

The instructor searches for contemporary cloud market-share estimates and compares AWS, Azure and Google Cloud. Since search results and percentages change, figures viewed during the lecture should not be used as permanent facts. He then navigates Azure web pages and explains pay-as-you-go versus the introductory free-account offer, credit limits, and a trial period. He recommends coordinating account signup with the practical class schedule so promotional resources remain available while students perform exercises. The instructor plans to demonstrate registration in a subsequent class. Promotional credit amounts, payment-card eligibility, trial length and free-tier services are time-sensitive and should be verified on Microsoft's current pages before signing up or spending money.

## 13. Azure Regions, Data Centers and Facility Tours

**Transcript reference:** Lines 575–672

The instructor uses an Azure infrastructure/regions map to talk about geographical placement of data centers, planned and existing regions, and redundancy options. He navigates through examples in India, discusses facility location, data center design and cooling, then shows visual references and 3D tours, including an undersea data-center concept and power/cooling ideas. The key lesson is that an Azure region is a geographic deployment choice and that availability, latency, data residency, resiliency and disaster-recovery design should influence region selection. The lecture includes illustrative region dates and site claims that require independent verification before being used as current facts.

## 14. Closing, Learning Sequence and Next Class

**Transcript reference:** Lines 663–704

The instructor points students to extra data-center materials and a visual tour, then closes by restating that the initial week covers core fundamentals before deeper Azure portal exercises. The expected next stage is account registration and learning to use Azure resources. Students should retain the business scenario, server role context, cloud deployment types, cost model and responsibility model as the conceptual foundation before starting practical deployments.

## Classroom examples preserved

- Nadeem/Khalid diamond-business owners; instructor as infrastructure administrator
- On-prem data center with cooling, redundant electricity, server/network buffer capacity
- ₹1 crore CAPEX and ₹20 lakh/month OPEX as **illustrative** cost figures
- Delhi-to-Bengaluru disaster-recovery scenario with RTO/RPO
- 16 GB / four-core physical-server expansion example
- Consolidating many workloads onto fewer virtualization hosts
- Buying an airline seat instead of buying an airplane to explain cloud consumption
- Using multiple providers and on-prem/private resources in deployment decisions
- Azure free-trial signup timing relative to class labs
- Azure region map and data-center visual tour

## Fidelity and verification notes

The detailed teaching narrative is preserved by topic but filler, repeated acknowledgments and minute-by-minute dialogue are not reproduced in these notes. For every original exchange, use `Original_Transcript/AZ-104-day-02.txt`. Technical corrections are explicitly separated and should not be attributed to the instructor.
