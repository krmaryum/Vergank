# VMware Class — Interview Questions & Answers (English)

**Class date:** 21 November 2026  
**Basis:** VMware-11-21-2026.txt (class transcript); questions organized by class topics.  
**Scope:** Interview preparation after the full lecture; distinct from the faithful classroom transcription.  
**Total questions:** 39

> Technical clarification: Answers are interview-ready explanations grounded in the lecture scenarios, with corrections of misleading technical statements made explicit in the notes below. They are not verbatim instructor quotations.

## 01 — Foundations and Clusters

### Q1. What are the four core resources required by a virtual machine?

**Answer:** Compute (vCPU), memory (RAM), a network adapter/port group, and storage. During OS installation you normally attach an ISO or another bootable deployment source. In this class the instructor asked the group to identify these four resources before creating a VM.

### Q2. What is ESXi responsible for and what does a datastore provide?

**Answer:** An ESXi host runs VMs and supplies CPU scheduling, memory, virtual networking and access to storage. The VM files live on a datastore, which may be backed by local disks, shared SAN/NAS or an eligible vSAN configuration. The instructor used four ESXi hosts in a cluster.

### Q3. What is a vCenter datacenter and a cluster?

**Answer:** A datacenter is a logical inventory container in vCenter. A cluster groups ESXi hosts so that supported features, such as HA and DRS, can coordinate their capacity and workloads. Neither object is automatically a separate physical building.

### Q4. How do HA, DRS and vMotion differ?

**Answer:** HA detects eligible host failures and restarts affected VMs on surviving hosts. DRS recommends or automates placement and workload balancing based on its configuration. vMotion is the live migration technology for a running VM under supported conditions. Host failure recovery by HA is not a live vMotion.

### Q5. Does HA guarantee zero interruption?

**Answer:** No. Failure detection, capacity checks and powering the VM back on take time. Interviewers expect you to distinguish service availability objectives from a guarantee of zero downtime, and to verify network and storage access on the surviving hosts.

### Q6. What is the relationship between NFS, SAN and vSAN?

**Answer:** They are different storage approaches. NFS is a file-sharing protocol commonly used for NAS datastores; SAN commonly exposes block LUNs; vSAN pools eligible host-local storage into a distributed datastore. This lecture referenced these options while choosing VM storage.

## 02 — Virtual Networking

### Q7. What is a vSphere Standard Switch (vSS)?

**Answer:** A vSS is configured independently on an ESXi host. It connects VM port groups and/or VMkernel services to host physical adapters. If multiple hosts use separate vSS instances, you must keep their port-group names, VLANs and physical connectivity consistent yourself.

### Q8. What is a vSphere Distributed Switch (VDS)?

**Answer:** A VDS is centrally configured through vCenter and has host-level forwarding components on participating ESXi hosts. It makes configuration and policy management more consistent across hosts, but the physical network and VLAN paths still must be correct.

### Q9. Why was a VDS introduced in this class?

**Answer:** The instructor showed a VM that could move from host 2 to host 3, where a different uplink or network mapping might make its guest network unreachable. A consistent distributed networking design reduces host-to-host configuration drift.

### Q10. What is a distributed port group and how is it related to a VLAN?

**Answer:** A distributed port group is a logical connection point for VMs on a VDS. Administrators assign policies such as VLAN handling, teaming and security settings to it. A port-group name alone does not create a VLAN on the physical network; the end-to-end network must carry it.

### Q11. Why did the instructor create VMware Lab, Cloud Lab and Windows Lab networks?

**Answer:** They illustrated separate logical networks for different groups of workloads while using the same distributed-switch framework. A VM can be attached to one of these port groups, or can have additional vNICs for more than one network when justified by the design.

### Q12. What is an uplink on a distributed switch?

**Answer:** The VDS has logical uplink ports that are mapped to participating ESXi hosts’ physical NICs (vmnics). Setting an uplink count in a wizard does not create physical cabling; you must map adapters and verify switches and link state.

### Q13. Why might you configure two active uplinks?

**Answer:** Redundancy and/or traffic distribution. The result depends on teaming policy, link configuration, physical switches and available bandwidth. In class, the instructor reserved multiple uplink positions and used selected adapters for connections.

### Q14. What is a VMkernel adapter (vmk) and how is it different from a VM port group?

**Answer:** VMkernel adapters are host-facing IP interfaces for services such as management, vMotion or storage (as supported). VM port groups connect guest virtual NICs. A dedicated VMkernel interface is not normally required merely to make a guest-only VLAN available.

### Q15. What network separation was demonstrated?

**Answer:** The classroom diagram distinguished an ESXi management/core range, a storage network, and a new VM network (using example 192.168.x.x, 172.16.x.x and 10.x.x.x ranges). Separation can improve isolation, troubleshooting and policy control; subnets and VLAN IDs must be validated in the actual lab.

### Q16. What are the main steps for creating a VDS?

**Answer:** From vCenter Networking, create a distributed switch in the desired datacenter, choose a compatible switch version, configure logical uplinks, add distributed port groups, attach hosts, map host vmnics, and validate VLAN/uplink and VM connectivity. Take a configuration backup and plan management-network recovery before moving active adapters.

### Q17. How should you choose the VDS version?

**Answer:** Choose a version supported by the ESXi and vCenter releases that will participate, and verify feature implications. The instructor discussed mixed-release compatibility and retaining a lowest-common-feature level. Exact compatibility must be checked against the installed versions, not assumed.

### Q18. A VM is reachable on host 1 but unreachable after moving to host 3. What do you check?

**Answer:** Check destination port-group existence and name, correct VLAN ID, physical trunk allowance, uplink vmnic mapping, NIC teaming/failover, guest IP/subnet/gateway, and security policies. Compare source and destination before changing anything. Centralized VDS configuration alone does not fix a missing physical VLAN.

### Q19. How can a network change accidentally disconnect an ESXi host?

**Answer:** Removing or remapping the management vmnic, changing management VLAN or an incompatible uplink policy can cut vCenter connectivity. Keep out-of-band/console access, use staged migration, verify each host, and maintain an explicit rollback procedure.

## 03 — VM Creation and Compatibility

### Q20. What are the key steps in creating a new VM through vCenter?

**Answer:** Select the datacenter/cluster or host, give the VM an appropriate name, choose compute placement, select datastore, set compatibility and guest OS, allocate vCPU/RAM/disk, choose the correct port group, and review before finishing. The lecture demonstrated this flow after the VDS lab.

### Q21. Why should virtual hardware compatibility be considered before creating a VM?

**Answer:** Virtual hardware compatibility determines which hosts can support the VM’s device features. Choosing the newest option may constrain migration to older hosts. In class the instructor compared ESXi release families and VM hardware versions; verify each combination in the vendor compatibility documentation.

### Q22. What is DRS placement during VM creation?

**Answer:** With an appropriately configured DRS cluster, the system can recommend or select an eligible host based on available capacity and rules. Manual placement remains possible. DRS is not a substitute for checking storage visibility, networking and affinity rules.

### Q23. What is nested virtualization?

**Answer:** Running a hypervisor inside a VM and then running additional VMs under it. This class used Workstation → ESXi → guest VM. Extra nesting (for example installing Hyper-V inside the guest) depends on CPU virtualization exposure and supported configurations, and can add substantial resource and performance constraints.

### Q24. What does CPU or memory hot-add mean?

**Answer:** On supported guest OS, VM hardware and configuration, some vCPU or RAM increases can be applied without powering off. It is not mandatory or supported in every combination, and enabling hot-add can have compatibility/performance implications. The instructor demonstrated enabling these options.

### Q25. Can one VM have two virtual NICs on different port groups?

**Answer:** Yes. For example, one vNIC could join the VMware Lab port group and another the Cloud Lab port group, subject to security and routing design. The VM then needs suitable IP configuration and careful routing so it does not become an unintended bridge between segments.

## 04 — Storage and Disk Provisioning

### Q26. Explain thin provisioning with an example.

**Answer:** A virtual disk may present a 100 GB maximum size to the guest but consume less datastore capacity initially, growing as guest data is written. It saves initial capacity but creates risk if many thin disks grow and fill the datastore; monitor free space and alerts.

### Q27. What are thick lazy-zeroed and thick eager-zeroed disks?

**Answer:** Both allocate their disk capacity up front. Lazy-zeroed typically zeros blocks when first used; eager-zeroed writes zeros during creation. Actual availability and requirements depend on disk type, datastore and vSphere version. The class compared these with thin disks.

### Q28. When might you choose thick versus thin?

**Answer:** Thin can help with flexible capacity planning in monitored environments; thick can simplify reservation and some workload requirements. Decide based on operational standards, datastore type, performance/availability requirements and actual capacity. Avoid assuming that thin always means better performance or free storage.

### Q29. How do you add a new virtual disk to an existing VM?

**Answer:** Edit the VM settings, add a new hard disk, set capacity, datastore and provisioning type, then confirm. Inside the guest OS, rescan disks and initialize/partition/format as appropriate. Check that you selected a new blank disk, because formatting an existing data disk is destructive.

### Q30. What is Raw Device Mapping (RDM)?

**Answer:** RDM is a mapping that lets a VM access a raw block LUN while maintaining a mapping file. It is different from putting an ordinary VMDK on a VMFS datastore and from thin/thick provisioning. In modern designs, verify whether an RDM is required and supported for the workload.

### Q31. What is Storage vMotion?

**Answer:** Storage vMotion changes the datastore location of a VM’s virtual disks under supported conditions, often while the VM is running. Compute vMotion moves running compute execution to another host; storage and compute migrations have different prerequisites.

### Q32. Can you convert a virtual disk from thin to thick or thick to thin?

**Answer:** Conversion is supported in certain migration/clone or disk operations, depending on platform and datastore. The instructor discussed provisioning conversion during storage changes. Do not promise zero downtime universally; validate the exact method and available capacity first.

### Q33. What should you check when a datastore is missing from an ESXi host?

**Answer:** First inspect the storage adapter/controller, rescans, detected devices, paths, LUN presentation, VMFS mounts, connectivity, and host logs. If nested in Workstation, verify the virtual disk/controller is actually attached. Do not jump directly to reinstalling or resetting the host.

### Q34. Why is Reset System Configuration risky?

**Answer:** It removes the host configuration and can disconnect the host and its networking/storage settings. Although the instructor showed the option during datastore discussion, in production it is a disruptive recovery operation requiring backup, maintenance approval and a rebuild plan.

## 05 — Identity and Operations

### Q35. Why would an administrator integrate vCenter with Active Directory?

**Answer:** To allow centrally managed directory identities to sign in to vCenter and then receive vSphere roles and permissions. Authentication integration does not automatically grant every AD user admin privileges. Supported options vary by vCenter release and identity provider.

### Q36. What prerequisites should be checked before AD identity integration?

**Answer:** Validate domain DNS resolution, domain controller reachability, clock synchronization, TLS/certificates where required, correct account permissions, and release-supported identity-source method. The lecture used a lab domain resembling VCPLAB.com; do not paste passwords into notes or GitHub.

### Q37. Why is DNS important for vCenter and AD authentication?

**Answer:** Directory and identity services often depend on consistent name resolution to discover domain controllers and verify endpoints. Wrong DNS records or a misconfigured resolver can cause timeouts, login failures and confusing errors even when IP connectivity works.

### Q38. What evidence should you capture for a VDS and VM deployment lab?

**Answer:** Document topology, host vmnic-to-uplink maps, VLAN IDs, distributed port groups, host and guest IP subnets, VM placement, datastore and disk provisioning, connectivity tests, and any vCenter tasks/errors. Include screenshots and a rollback plan, but redact passwords and tokens.

### Q39. What is the best way to explain this class in an interview?

**Answer:** Describe the scenario: four ESXi hosts in a vCenter cluster, separate management/storage/VM networks, a central VDS with distributed port groups and uplink mapping, then VM creation and storage choices. Explain why consistent VLAN reachability matters for migration. Finish with how you validated the network, datastore and AD access.

---

## Technical clarification (not a transcript rewrite)

- **vCPU** means virtual CPU, not “vSphere CPU.”
- **HA** restarts affected VMs after host failure; it does not live-migrate a VM from a failed host.
- **VMkernel** adapters serve ESXi host services; a guest VM port group does not inherently need its own vmk IP.
- **VDS** consistency does not replace correct physical-switch VLAN trunks and vmnic mappings.
- **Disk provisioning:** thin and thick describe virtual disk allocation; RDM is a separate mapping model.
- **Destructive actions:** never treat ESXi Reset System Configuration as the first datastore troubleshooting step.
- **Compatibility:** verify exact vSphere/ESXi and virtual hardware combinations against the version in use.
- **AD integration:** supported identity source/federation methods vary by version; keep credentials outside GitHub.

### Source

Original lecture: `VMware-11-21-2026.txt` (included unchanged in the ZIP).
