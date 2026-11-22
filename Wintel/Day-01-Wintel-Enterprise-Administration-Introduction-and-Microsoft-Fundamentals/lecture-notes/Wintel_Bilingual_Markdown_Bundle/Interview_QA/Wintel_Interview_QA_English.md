# Wintel Lecture — Interview Questions & Answers (English)

**Coverage:** Wintel lecture Parts 1–3, approximately original transcript lines 1–496. **Not** the remaining lines 497–835.

**How to use:** Read each answer, then practice a 45–90-second spoken explanation. The lecturer’s training examples are marked as examples; a few safety/technical clarifications use standard professional terminology and are not presented as verbatim lecturer quotations.

**Source:** `wintel.txt` and existing bilingual Parts 1–3 notes. The Q&A are newly authored for interview practice, not a word-for-word transcript.


## Wintel and Server Fundamentals

### Q1. What does Wintel mean in an enterprise infrastructure context?

**Answer:** Wintel traditionally refers to Microsoft Windows running on Intel-compatible x86 hardware. In the lecture, it introduces the combination of Windows Server software and server hardware, including AMD-based platforms commonly used today.

### Q2. Does a server have to be dedicated server hardware?

**Answer:** No. A server is a system that delivers a service to clients. The instructor used a laptop or desktop sharing a printer and application files as examples. Dedicated enterprise hardware is chosen for performance, resilience, and manageability.

### Q3. How does the cybercafé print-server example work?

**Answer:** A printer is attached to one computer on a network. Other computers send print jobs to the shared printer through that machine. The example demonstrates the server/client relationship without requiring a separate physical server.

### Q4. What is the purpose of a file-transfer server in the instructor’s example?

**Answer:** The administrator downloads common installers once and stores them centrally. Users on other networked PCs retrieve those installers from that system. This reduces repeated downloads and helps when internet connectivity is unavailable.

### Q5. What does FTP stand for, and how is it different from SFTP?

**Answer:** FTP stands for File Transfer Protocol and does not encrypt credentials or data by default. SFTP is SSH File Transfer Protocol and transfers files over an encrypted SSH connection. The lecture discusses downloading and uploading; the transfer direction does not decide whether FTP or SFTP is used.

### Q6. What is the difference between HPE, Dell, Lenovo, Intel, and AMD in a server discussion?

**Answer:** HPE, Dell, and Lenovo sell branded server systems and support solutions; Intel and AMD provide processors used in many of those servers. The class uses this distinction to explain the server supply chain. Vendor component sourcing is broader than CPUs alone.


## Enterprise Teams and Identity Services

### Q7. Why should a Wintel engineer understand multiple IT teams?

**Answer:** A real deployment involves physical servers, storage, virtualization, operating systems, networking, and security. The instructor assigned these responsibilities to different students to show how an architect coordinates people and dependencies.

### Q8. What were the team roles in the class scenario?

**Answer:** The example assigned Nadeem to storage, Khalid to virtualization, Sarfraz to physical servers, Anil to operating systems, and the instructor to the data-center architect role. It was a teaching scenario, not a claim about permanent employment duties.

### Q9. What does identity and access management accomplish?

**Answer:** IAM ensures that users can be identified, authenticated, and granted appropriate permissions. In the instructor’s company scenario, services such as Active Directory Domain Services support centralized user and access management.

### Q10. Why might an internal company need AD DS, DNS, and DHCP?

**Answer:** AD DS organizes domain identities; DNS resolves names needed to locate domain and application services; DHCP can assign network configuration automatically to clients. The lecture lists them as foundational enterprise services.

### Q11. What is the role of HTTPS and a certificate authority?

**Answer:** HTTPS protects web connections through TLS. A certificate authority issues or signs certificates that help clients establish trust in a server identity. The instructor mentions a CA as part of the company’s service design; a public-facing site generally needs certificates trusted by its visitors.

### Q12. What does “resource” mean in an IT service project?

**Answer:** In the class, resource is used broadly for people, systems, capacity, and other assets needed to deliver work. An architect plans which resources are needed, when, and at what cost.


## Production Server Builds and SLAs

### Q13. Why is server build not the same as operating-system installation?

**Answer:** An enterprise build includes hardware preparation, remote-management access, RAID or storage configuration, firmware updates, OS deployment, network configuration, monitoring, security controls, patching, and validation. Merely installing Windows is only one stage.

### Q14. What is iLO and why would an administrator use it?

**Answer:** HPE iLO is an out-of-band management interface used to inspect and control supported servers remotely, including tasks such as console access and power actions. The lecture includes iLO in its example build checklist.

### Q15. What is RAID and where does it fit in the build process?

**Answer:** RAID combines physical disks into logical storage arrangements for redundancy, performance, or both depending on level. The instructor places RAID setup before OS deployment in a typical production build.

### Q16. Why are firmware upgrades part of a server build?

**Answer:** Firmware controls platform components such as BIOS/UEFI, controllers, and adapters. Updating to an approved version can address compatibility, reliability, and security issues. In production this must follow change and vendor-compatibility procedures.

### Q17. What does an eight-hour server-build SLA mean?

**Answer:** In the instructor’s example, the team has an eight-hour service-level target or window to complete the request. It includes coordination, interruptions, reboots, and buffer time; it does not mean Windows installation itself takes eight hours. Actual SLAs differ by organization.

### Q18. Why can a production server reboot take longer than a desktop reboot?

**Answer:** Enterprise servers may perform firmware checks, controller initialization, hardware self-tests, and post-patch processing. The lecture notes that some patch-related restarts can consume 10–20 minutes, so admins plan accordingly.

### Q19. What should you do if competing incidents put your build SLA at risk?

**Answer:** Communicate early, document current status, and arrange a clear handover or escalation so another team member can continue. The instructor emphasizes coordination to avoid an SLA breach.


## Enterprise Project and Capacity Planning

### Q20. What questions should an architect ask after a customer requests 1,500 servers?

**Answer:** Clarify workload purpose, physical-versus-virtual split, cloud footprint, hardware sizing, storage, network, security, availability, disaster recovery, location, budget, and timeline. The class begins with the server count and then broadens into these design decisions.

### Q21. How did the instructor split the 1,500-server example?

**Answer:** The illustrative split was about 200 physical servers, 800 virtual servers, and 500 cloud servers—1,500 total. This was a classroom planning example, not a recommended universal ratio.

### Q22. Does a request for 1,500 servers mean buying 1,500 physical machines?

**Answer:** No. Many server instances may run as virtual machines on a smaller number of physical hosts, and others may run in a cloud environment. Exact host quantities depend on capacity, resilience, performance, and licensing.

### Q23. Why should server administrators understand the whole data center?

**Answer:** A server depends on power, cooling, racks, networking, storage, access control, monitoring, and support processes. A cross-team view helps an administrator diagnose incidents and coordinate recovery.

### Q24. What is the difference between on-premises, virtualized, and cloud deployments?

**Answer:** On-premises identifies who operates the physical site; virtualization identifies how compute is partitioned into virtual machines; cloud identifies a service-delivery and operating model. These categories can overlap—a company can run virtual machines on-premises and in cloud.

### Q25. What is the relevance of PMP, PRINCE2, and ITIL in the lecture?

**Answer:** The instructor introduces them while discussing project acquisition, delivery, and service management. PMP and PRINCE2 relate to project management; ITIL is a framework for IT service management. Their exact purpose should not be reduced to only marketing or client transparency.


## Colocation, Support and Operations

### Q26. What is data-center colocation?

**Answer:** Colocation means placing customer-owned or leased equipment in a third-party facility that provides space, power, cooling, connectivity, and physical infrastructure. The lecture uses public data centers in Noida and an overseas customer scenario to illustrate the option.

### Q27. What should you check before choosing a colocation provider?

**Answer:** Evaluate uptime commitments, redundant power and cooling, connectivity, physical security, remote hands, access procedure, support response times, location risk, compliance, and total cost. The lecturer emphasizes visiting or reviewing the proposed setup before committing.

### Q28. Can every engineer enter a third-party data center?

**Answer:** Not necessarily. Entry is typically restricted to approved personnel through identity checks and provider procedures. The lecture discusses exceptions for authorized visits, inspections, and supervised vendor work.

### Q29. How are physical faults addressed when admins work remotely?

**Answer:** The administrator collects evidence remotely, opens a support case, coordinates with the OEM or facility remote-hands team, arranges authorized access, and verifies the repair. This fits the lecture’s remote operations and vendor-support examples.

### Q30. Why are hardware support contracts important?

**Answer:** Enterprise equipment can fail; support contracts define access to replacement parts, vendor engineers, and response arrangements. The instructor used a five-year support term as an example; contract length depends on purchasing decisions.

### Q31. Why might staffing decrease after a deployment goes live?

**Answer:** Build and migration stages may need a larger temporary team; steady-state operations can need fewer people if monitoring, provider services, and maintenance processes are established. The lecture discusses contract staffing and 24×7 coverage.


## Disaster Recovery and Interview Scenarios

### Q32. What is the difference between a primary site and a DR site?

**Answer:** The primary site normally runs production workloads. A disaster-recovery site provides resources and procedures to restore or continue critical services if the primary site becomes unavailable. The instructor used geographically separate locations for illustration.

### Q33. What is RTO?

**Answer:** Recovery Time Objective is the maximum targeted duration to restore a service after disruption. For example, an RTO of four hours means the organization aims to restore that service within four hours.

### Q34. What is RPO?

**Answer:** Recovery Point Objective is the maximum targeted amount of data loss measured in time. An RPO of fifteen minutes means recovery design aims to avoid losing more than about fifteen minutes of data changes.

### Q35. What is the difference between backup, high availability, and disaster recovery?

**Answer:** Backup is a recoverable copy of data, HA reduces interruptions from component failures, and DR provides recovery when larger services or sites fail. They complement rather than replace one another.

### Q36. Why should an organization conduct DR drills?

**Answer:** A DR plan that has never been tested may fail when it is needed. Drills validate recovery procedures, dependencies, communication, RTO/RPO feasibility, and the readiness of personnel. The lecture includes DR drills as part of planning.

### Q37. How would you answer an interview question: “Tell me your approach to a new data-center project”?

**Answer:** First confirm business and application requirements. Then estimate capacity and server types, choose site/colocation and resiliency model, plan networking/storage/security, define build and vendor ownership, agree SLAs and RTO/RPO, execute phased deployment, test, document, and hand over to operations. These stages synthesize the instructor’s scenario into a sample interview response.


## Additional interview practice (new exercises)

1. Explain how you would document the acceptance checklist for a server build.
2. Draw a simple on-premises architecture for the 1,500-server *illustrative* scenario.
3. Describe the first five checks you would perform when an ESXi or Windows server becomes unreachable.
4. Draft a DR runbook with owners, prerequisites, communication steps, and evidence of successful recovery.

*These exercises are additional study suggestions, not direct classroom questions.*
