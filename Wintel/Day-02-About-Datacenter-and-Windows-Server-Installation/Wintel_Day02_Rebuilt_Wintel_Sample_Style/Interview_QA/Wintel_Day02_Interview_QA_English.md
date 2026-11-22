# Wintel Day 02 — 35 Interview Questions & Answers (English)

Based on the Day 02 class themes; answers incorporate separately identified best-practice clarifications where needed. Interview preparation is **additional material**, not words attributed to the instructor.

## Q01. Can a laptop or desktop act as a server?

**Answer:** Yes. A server is defined by the services it provides. A desktop can host a web server, file share, or printer service. Production reliability requirements may justify dedicated server-class hardware.

## Q02. Why does server downtime matter to a business?

**Answer:** A failed service can stop customer operations, reduce revenue, delay work and damage trust. The lecture uses banking and ecommerce examples.

## Q03. How do you compare tower and rack servers?

**Answer:** Tower servers use freestanding chassis and are often convenient in small environments. Rack servers are designed for standardized racks and higher-density centralized operation; either can serve enterprise workloads depending on configuration.

## Q04. What is a redundant power supply?

**Answer:** A system with correctly configured dual PSUs and independent power paths can remain powered if one PSU or feed fails, within the supported design limits.

## Q05. What is RAID and does every RAID level protect against disk failure?

**Answer:** RAID combines drives for performance, capacity, or redundancy depending on the level. RAID 1 and many parity-based levels tolerate specified failures; RAID 0 has no redundancy. RAID is not a backup.

## Q06. What should you check when a RAID drive fails?

**Answer:** Check array health and alerts, identify the failed physical drive precisely, confirm backups and hot-swap support, replace according to the runbook, and monitor rebuild completion.

## Q07. What is out-of-band server management?

**Answer:** A dedicated management controller or interface lets an authorized administrator inspect hardware, open remote console, and manage power independently of the guest operating system.

## Q08. A patched Windows server is not reachable by RDP. What do you do?

**Answer:** Check monitoring and network reachability, open the management console, inspect boot/patch state and hardware alerts, correlate change logs, then use a controlled reboot only when justified.

## Q09. What is the difference between a PSU and PDU?

**Answer:** PSU converts and regulates power inside the server. A PDU distributes electrical power to multiple devices in a rack.

## Q10. What is a rack unit?

**Answer:** One rack unit (1U) is a standard vertical height of 1.75 inches. A 2U server consumes two units of rack height.

## Q11. Can a 42U rack always hold 42 servers?

**Answer:** No. Server heights vary, and space may be needed for switches, PDUs, cable management, airflow considerations, and other equipment.

## Q12. Should you always leave 1U between rack servers?

**Answer:** No universal rule requires that. Follow the chassis and rack vendor airflow guidelines; empty gaps may need blanking panels to maintain airflow.

## Q13. How do tower servers support small businesses?

**Answer:** They can host file, print, directory or application services with lower infrastructure complexity and no full-size rack requirement, if the capacity and uptime needs fit.

## Q14. What factors drive server hardware selection?

**Answer:** Workload, CPU and RAM sizing, storage performance, network connectivity, redundancy, remote management, warranty, lifecycle, support and total cost.

## Q15. What is a blade server?

**Answer:** A blade server is a modular compute unit installed in a chassis sharing some infrastructure such as power, cooling and management.

## Q16. What are shared-chassis failure domains?

**Answer:** Failure of a shared blade chassis component can affect several blades. Redundant components and recovery planning reduce but do not eliminate that risk.

## Q17. What is server lifecycle management?

**Answer:** Planning procurement, deployment, monitoring, maintenance, refresh, migration and secure retirement based on support agreements and business needs.

## Q18. What is secure decommissioning?

**Answer:** Remove the system from service, preserve required records, revoke access, sanitize or destroy data-bearing media according to policy, and document disposal.

## Q19. Why is ordinary disk formatting insufficient for sensitive data disposal?

**Answer:** Formatting may leave recoverable information. Use an approved sanitization or destruction method appropriate to the media.

## Q20. Can you build a Windows Server lab without purchasing a physical server?

**Answer:** Yes. VMware Workstation on an adequately sized host can run Windows Server VMs for many administrative exercises; complex multi-VM scenarios need more resources.

## Q21. What are host and guest in virtualization?

**Answer:** The host is the underlying computer and hypervisor environment; the guest is the operating system running within the virtual machine.

## Q22. Why should VM memory be allocated carefully?

**Answer:** VMs draw from finite host memory. Overcommit or excessive active demand can slow guests and destabilize the host.

## Q23. When would you install Windows Server on bare metal instead of a VM?

**Answer:** Bare metal may fit certain performance, hardware-control or architectural requirements. VMs are often preferred for flexible labs and consolidation.

## Q24. Why use an ISO image?

**Answer:** An ISO contains installation media that a VM can mount as a virtual optical drive, or that can be used to prepare bootable physical media.

## Q25. What is Rufus used for?

**Answer:** Rufus helps create bootable USB installation media from supported disk images. Choosing the correct target device matters because it can be erased.

## Q26. What is UEFI?

**Answer:** UEFI is modern firmware that initializes hardware and boots an operating system. Installation media and partition scheme must be compatible with the intended boot mode.

## Q27. What do you select in VMware Workstation New VM wizard?

**Answer:** Installation ISO, guest OS family/version, VM name/location, vCPU, RAM, virtual disk and network settings. Review before powering on.

## Q28. Why separate operating system and data disks?

**Answer:** Logical separation can simplify capacity management, backups, recovery planning and testing, although it does not inherently create redundancy.

## Q29. What is Windows Server Core?

**Answer:** Server Core is a minimal installation option without the full Desktop Experience GUI, typically managed with PowerShell and remote administration tools.

## Q30. How does Desktop Experience differ from Server Core?

**Answer:** Desktop Experience provides the full GUI; Core has less local GUI surface and different management workflow. Choice depends on workloads and support requirements.

## Q31. A VM does not boot from the attached Windows Server ISO. What would you check?

**Answer:** Confirm ISO integrity and attachment, virtual CD/DVD connection, firmware/boot order, guest compatibility and any boot prompts; avoid destructive changes while diagnosing.

## Q32. What is Microsoft Intune in the context of this lecture?

**Answer:** It is a Microsoft endpoint management service mentioned while discussing device policies, updates and administration; it is not the same product as AD DS.

## Q33. How would you describe your home lab in an interview?

**Answer:** State the host specifications, virtualization software, VM roles, network layout, configuration evidence, verification steps and any troubleshooting you personally performed.

## Q34. What should be recorded after a server deployment lab?

**Answer:** Objective, prerequisites, VM hardware, OS edition, install steps, screenshots, verification, issues, fixes and safe cleanup procedure.

## Q35. What should you do before a forced remote reboot?

**Answer:** Check whether the machine is running updates or a critical task, evaluate impact, follow change/incident policy and prefer graceful recovery when possible.

