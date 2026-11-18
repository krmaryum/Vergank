# AZ-104 Day 02 — Technical Verification & Corrections

> **Separate from the original lecture:** These notes correct or qualify claims so study materials do not accidentally teach inaccuracies. They do not rewrite the instructor's words in the source transcript.

1. **RTO vs RPO:** RTO is the desired time to restore service. RPO is the acceptable amount of lost data measured backward in time. The lecture's one-hour-old data example describes RPO, not automatically RTO.
2. **Hybrid vs multi-cloud:** On-premises/private + public cloud is hybrid. Azure + AWS alone is multi-cloud, unless there is also a qualifying private cloud arrangement.
3. **Cloud bills at shutdown:** A stopped VM may no longer incur compute charges if deallocated, but disks, snapshots, networking, reserved services and other items may continue billing. Not all resources stop charging with a click.
4. **Server hot-add:** VM RAM/vCPU hot-add depends on hypervisor version, settings and guest OS; Type 1 does not imply guaranteed zero-downtime resizing. Storage expansion also varies.
5. **Cooling and design temperatures:** The cited 15–16 °C is a classroom example, not a universal required data-center temperature. Follow equipment and engineering guidance.
6. **Ozone and climate:** Ozone-layer depletion and greenhouse-driven global warming are distinct environmental mechanisms. Virtualization may improve energy efficiency; the lecture's causal explanation oversimplifies these topics.
7. **Cloud origins/NIST:** NIST is a standards body, not a cloud service seller; the transcript's specific early-development and provider partnership chronology needs source verification before repeating as fact.
8. **RAID terminology/history:** RAID is a storage organization/redundancy technology; it should not be presented as equivalent to the entire category of storage virtualization or as an undisputed first virtualization technology.
9. **Cloud registration/payment:** Azure eligibility, accepted cards, credit value, currency, and free duration depend on current offer and country; do not treat the instructor's example charges as universal.
10. **Reliability/security:** Public cloud availability, default public IPs, automatic scaling and built-in DR depend on selected services and explicit customer configuration; none is guaranteed for every resource.
11. **Market share and provider claims:** Search result counts and percentages shown during class are transient, and vendor-specific assertions require dated citations to be current.
12. **Shared responsibility:** SaaS/PaaS/IaaS shift different obligations, but identity configuration, access governance, data classification and protection remain customer responsibilities to varying degrees.
13. **Windows web server name:** The instructor transcript appears to say IAS for web services. Microsoft's web-server role is **IIS (Internet Information Services)**; IAS historically referred to Internet Authentication Service.
14. **Provider technologies:** VMware Cloud Foundation is a platform for private/hybrid cloud, not simply a consumer public-cloud service of the same type as Azure or AWS.

## Verification checklist for future sessions
Confirm account offers, regional availability, pricing, compliance requirements and live market conditions against up-to-date official Microsoft and provider sources before implementing a lab or making a purchasing decision.
