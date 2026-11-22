# Wintel Day 03 — Technical Verification and Context

This file is **separate from the instructor's words**. The original recording is preserved without silently editing technical statements.

1. **VMware Tools configuration:** `Complete` is an available install choice, not a universal production best practice. Guest features, host–guest copy/paste and file transfer should follow security requirements.
2. **Change window versus SLA:** A service-level agreement (SLA) measures service commitments; an approved **change window** is the authorized time for performing change work. They are related but not interchangeable.
3. **Type 1 versus Type 2:** VMware Workstation is a hosted Type 2 hypervisor; ESXi is a Type 1 bare-metal hypervisor. Microsoft Hyper-V architecture is not accurately described merely by comparing the usability of their interfaces.
4. **Server memory requirements:** Requirements differ by Windows Server release, install option and deployed roles. The instructor's statement about 512 MB for current server editions is not a safe generic sizing rule. Use vendor minimums and workload testing.
5. **POST and firmware:** POST runs under platform firmware. BIOS and UEFI firmware are responsible for hardware initialization and launching the boot path; they are not conventional 'mini operating systems' in the same sense as a general-purpose OS.
6. **RTC/CMOS battery:** RTC battery failure can cause the clock or some settings to reset on some systems. Many modern UEFI configurations store settings in nonvolatile flash. Replacing a CMOS battery annually is not a universal server-maintenance requirement.
7. **Out-of-band management:** HPE iLO and Dell iDRAC may remain reachable when the OS is down, but not through all motherboard, BMC, power or network failures.
8. **Hardware replacement warranty:** Vendor support response time and coverage depend on a purchased contract and service-level conditions; no universal five-year or seven-year maximum exists.
9. **Blade enclosure shutdown:** Operating system shutdown does not necessarily remove enclosure power; the proper procedure is vendor- and cluster-specific. An enclosure may host multiple active systems, so it must not be powered off casually.
10. **Secure Boot:** Secure Boot checks signed boot components when enabled and supported. It does not mean that the whole system's software is proven safe, and it is different from BIOS/UEFI administrator passwords.
11. **Troubleshooting order:** Prefer read-only evidence gathering, vendor documentation and backup/rollback planning before changing firmware, storage controllers, BCD settings or cluster state.
