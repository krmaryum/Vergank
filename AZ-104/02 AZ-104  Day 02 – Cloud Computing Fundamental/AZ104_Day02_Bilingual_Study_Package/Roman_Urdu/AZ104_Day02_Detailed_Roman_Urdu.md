# AZ-104 — Day 02 | Detailed Roman Urdu Class Notes

> **Type:** Topic-organized detailed notes based on the uploaded classroom transcript. These are NOT a complete line-by-line translation. The unchanged 704-line transcript is included in the ZIP for full fidelity. Technical corrections are in a separate file.

## Source coverage

Full transcript reviewed: lines 1–704. Notes follow the original lecture order and preserve the major teaching examples, questions, scenarios and discussions.

## 01. Role of an Infrastructure Administrator

**Transcript reference:** Lines 1–9

Instructor Day 01 ka revision karte hain aur kehte hain ke poore course ko sirf VM, networking ya storage ki ek job samajh kar na parhein. Apne aap ko company ka **infrastructure administrator** samjhein. Kabhi VM create karni hogi, kabhi server, network, storage, OS, application service ya troubleshooting karni hogi. Cloud computing ko samajhne ka maqsad in sab cheezon ke aapas ke connections samajhna hai. Yahan sirf Azure portal ke buttons nahi seekhne; business requirements aur real operations bhi samajhne hain. Instructor pichhli class ke data center aur ticketing tool discussions ko bhi refer karte hain.

## 02. On-Premises and Why Organizations Need Servers

**Transcript reference:** Lines 10–42

Nadeem batate hain ke **on-premises** mein physical/bare-metal servers, racks, network aur doosra hardware company ki jagah par hota hai. Instructor is ko services se connect karte hain: **DHCP** devices ko automatically IP configuration deta hai; **DNS** names resolve karta hai; **AD DS** users aur identities centrally manage karta hai; aur web servers websites/applications chalate hain. Pehle employees desktops par baith kar kaam karte thay; laptops se remote working mumkin hui. Agar 500 computers hon to sab par manually IP lagana mushkil aur error-prone hota hai. Critical services ke liye multiple servers rakhe jaate hain taake ek failure se poori service band na ho. Instructor wazeh karte hain ke iss session mein Windows Server ke har role ko deep dive mein nahi parhenge; focus cloud ka foundation hai.

## 03. The Diamond-Business Data Center Scenario

**Transcript reference:** Lines 43–52

Teacher ek scenario dete hain: **Nadeem aur Khalid UAE mein diamond business ke owners** hain aur instructor ko pehla infrastructure administrator hire karte hain. Business ke users, website aur applications ke liye IT setup banana hai. Administrator sab se pehle proper **data center** maangta hai: cooling, redundant power, UPS/generator, physical servers, future growth ke liye extra capacity, routers, switches, firewalls, load balancers, licenses aur maintenance staff. Agar aaj 5 servers chahiye hon to future requirements aur failure ko dekh kar 6–7 servers plan karne ka example diya gaya. Agar saat core services hon, to redundancy ke saath deployed instances ki tadaad zyada ho sakti hai. Lecture mein bataya gaya temperature aur servers ki exact tadaad universal standard nahi, **classroom estimates** hain.

## 04. CAPEX and OPEX for Traditional IT

**Transcript reference:** Lines 52–80

Diamond business ke example mein teacher estimates dete hain: ek physical server taqreeban **₹10 lakh**, sample networking set **₹8 lakh**, aur initial data center investment qareeban **₹1 crore**. Is upfront investment ko **CAPEX — Capital Expenditure** kaha. Administrators ki salaries, electricity, cooling, repair, maintenance, licenses aur regular bills **OPEX — Operating Expenditure** hain. Instructor hypothetical **₹20 lakh per month** ka OPEX bhi batate hain. Yeh figures exact market quotation nahi; sirf ownership aur cost ka difference samjhane ke liye class examples hain.

## 05. Disaster Recovery, RTO, and RPO

**Transcript reference:** Lines 81–145

Agar earthquake, building access problem ya facility failure se primary data center down ho jaye to company ki services ruk sakti hain. Teacher is liye alag geographical jagah **DR — Disaster Recovery** site ka concept dete hain; example **Delhi primary** aur **Bengaluru DR** hai. Critical applications ko DR par rakhna pad sakta hai, lekin is se cost barhti hai. **RTO** aur **RPO** introduce kiye jaate hain aur replication delay discuss hota hai. One-hour example mein DR copy production se purani ho sakti hai. Important clarification: **RTO = recover karne ka allowed time**, jabke **RPO = acceptable data loss ka time window**. Dono ek cheez nahi. Instructor yeh bhi kehte hain ke cloud ke baad bhi traditional on-prem data centers aur DR sites khatam nahi huay.

## 06. Limits of Physical-Server Expansion

**Transcript reference:** Lines 146–160

Traditional physical server par application grow karne lage to pehle di hui **16 GB RAM / 4 cores** kam pad sakte hain. Instructor example dete hain ke RAM 24 GB aur CPU 6 ya 8 cores karne ke liye old-style hardware upgrade mein shutdown aur downtime lena pad sakta hai. Is downtime se business impact hota hai. Asal lesson yeh hai ke initial sizing hamesha future load ke liye kafi nahi hoti. Kuch physical systems mein upgrades zyada flexible ho sakte hain, magar class ka comparison manual physical changes aur virtualized provisioning ke darmiyan hai.

## 07. Virtualization: Consolidation, Efficiency and Hypervisors

**Transcript reference:** Lines 160–211

**Virtualization** traditional IT aur cloud ke darmiyan important bridge hai. Teacher **server consolidation** samjhate hain: kai VMs kam physical hosts par chal sakti hain, jis se space, electricity, cooling aur kabhi CAPEX/OPEX kam hota hai. Is ko **Go Green** se relate kiya. **Type 1 / Type 2 hypervisors**, VMware Workstation, Broadcom ke baad VMware, Nutanix aur public-cloud integration par baat hui. Example mein 14 server workloads ko kam physical hosts par chalane ka zikr hai; actual capacity CPU, RAM, storage IOPS, availability aur workload sizing par depend karti hai. **Hot-add** har Type 1 platform mein automatically available nahi hota; VM settings aur guest OS matter karte hain. RAID aur virtualization history ke kuch claims ko technical verification mein alag rakha gaya hai.

## 08. Why Cloud Computing and the Airline Analogy

**Transcript reference:** Lines 211–234

Teacher **AWS, Microsoft Azure aur GCP** introduce karte hain. Sab se yaadgar example **airline ticket** hai: ek safar ke liye poora plane khareedna traditional data center ownership jaisa hai; existing flight mein ticket lena cloud shared infrastructure use karne jaisa hai. Aap physical servers khareede baghair resources consume karte hain; is ko **pay-as-you-go** aur elastic capacity se relate kiya gaya. Cloud ka matlab hardware gayab hona nahi: provider ke real data centers aur physical servers maujood hote hain. NIST aur providers ki historical dates instructor ke lecture ke claims hain; independently verified dates nahi.

## 09. Public, Private, Hybrid and Multi-Cloud Choices

**Transcript reference:** Lines 235–326

Instructor discuss karte hain ke workload kahan hona chahiye. **Public cloud** provider ka shared platform hai; **private cloud** ek organization ke liye dedicated environment; **hybrid cloud** on-prem/private environment ko public cloud se connect karta hai. Class mein Microsoft aur AWS dono par servers rakhne ka example aata hai: is ko zyada precisely **multi-cloud** kehte hain; sirf do public clouds use karna hybrid ki definition nahi. Students poochte hain ke public cloud ka server physical hota hai ya virtual. Jawab: provider ke paas real hardware hota hai, aur customer ko isolated virtual/service resources milte hain. Outage aur resilience discuss hui, lekin providers mein workloads divide karne se complexity aur cost bhi barh sakti hai.

## 10. Cloud Benefits, Security, Data Control and Risk

**Transcript reference:** Lines 327–448

Teacher cloud ke benefits batate hain: **fast provisioning**, vertical/horizontal **scalability**, possible **high availability**, networking services, updates/automation, backup, DR aur **faster time to market**. Saath risks bhi discuss hote hain: provider outage, external dependency, sensitive data kis ke control mein hai, identity compromise aur unauthorized access. Kuch critical workloads on-prem rakh kar **mixed environment** banana practical ho sakta hai. Important clarification: cloud mein security shared responsibility hai; customer ko IAM, access, networks aur data protection configure karni hoti hai. **VM band karne se hamesha bill zero nahi hota**—disks aur kuch network resources ka charge reh sakta hai.

## 11. Cloud Architecture and Service Models

**Transcript reference:** Lines 449–482

Class cloud types ke baad **front end/back end** aur **service models** discuss karti hai. **On-prem** mein hardware, storage, networking, virtualization, OS, middleware, runtime, applications aur data sab customer manage karta hai. **IaaS** mein provider physical infrastructure aur virtualization sambhalta hai, magar guest OS, apps, identities aur data ki zimmedari customer ki hoti hai. **PaaS** mein platform/runtime ka zyada kaam provider leta hai; developer application aur data par focus karta hai. **SaaS** ready application deta hai, lekin access, user settings aur data governance phir bhi important rehte hain. Instructor ka maqsad responsibilities ki layers samjhana hai.

## 12. Azure Provider Comparison and Account Overview

**Transcript reference:** Lines 483–574

Instructor cloud **market share** ka live search karke AWS, Azure aur GCP compare karte hain. Yeh percentages waqt ke saath change hoti hain, is liye lecture ki values ko permanent fact na samjhein. Phir **Azure pay-as-you-go** aur introductory **free account**, trial credit aur trial time discuss karte hain. Students ko mashwara dete hain ke account practical class ke qareeb create karein taake promotional resources labs ke liye available rahen. Registration ka demo next class mein plan hai. Credit amount, eligible cards, trial duration aur free services **time-sensitive** hain; signup se pehle current Microsoft terms check karein.

## 13. Azure Regions, Data Centers and Facility Tours

**Transcript reference:** Lines 575–672

Instructor **Azure regions/infrastructure map** se geographical data center locations, planned regions aur redundancy options dikhate hain. India ki locations ke examples, facility layout, cooling, 3D tours aur **undersea data center** concept bhi discuss hota hai. Main learning yeh hai ke **region selection** latency, data residency, availability, DR aur business needs ko affect karta hai. Lecture mein jo specific region launch dates aur sites batayi gayi hain unhein latest verified facts na samjhein.

## 14. Closing, Learning Sequence and Next Class

**Transcript reference:** Lines 663–704

Instructor additional data center material aur visual tour ka reference dete hain. Phir batate hain ke **first week** mein foundation clear ki ja rahi hai; baad mein Azure account aur portal ki practical exercises aayengi. Students ko diamond-business scenario, core server roles, cloud deployment types, cost model aur shared-responsibility samajh kar next class mein jana chahiye.

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
