# Instructor's Explanation vs Technical Best-Practice Clarifications

This file is deliberately separate from the original lecture. Statements below are clarifications, not silent modifications to what the instructor said.

1. **24×7 servers / end users:** Usage duration is not the formal definition of server versus client. A server provides services; a workstation typically consumes them. Both can operate continuously or intermittently.
2. **RAID:** RAID 0 provides no disk fault tolerance. RAID 1/5/6/10 have different redundancy and minimum-drive requirements. RAID is not a substitute for backups.
3. **Management ports:** Vendor management features often use iDRAC, iLO, IPMI/BMC or other interfaces. Avoid exposing them to the public internet; use restricted management networks, strong authentication and approved remote access.
4. **Reboot safety:** A hard reset during patching can cause corruption or interrupted updates. Inspect status and follow incident/change procedures first.
5. **Rack spacing:** Do not apply a blanket one-U-gap rule. Follow vendor airflow instructions and use blanking panels where needed.
6. **Rack capacity:** 42U specifies a vertical rack height, not a guaranteed number of devices.
7. **Refurbished equipment:** Hardware can be reused after approved media sanitization, but warranties, firmware support, power draw and noise must be assessed.
8. **Disk sanitization:** Formatting is not necessarily secure data destruction. Use recognized sanitization methods appropriate to SSD/HDD and company policy.
9. **Hardware prices/lifetimes:** Numbers and costs in the class are illustrative, not current quotes or universally guaranteed lifetimes.
10. **PSU/PDU:** PSU is a power supply unit; PDU is a power distribution unit. Their roles are different.
11. **Server Core:** Server Core is not the same product as Desktop Experience with GUI disabled; choose installation options based on current Windows Server documentation and supported pathways.
12. **Bootable USB:** Preparing bootable media may wipe the selected USB. Validate the device and ISO source.

**Sources:** These are general operational clarifications for study, not an externally audited product-version compatibility matrix. Confirm platform-specific procedures in vendor documentation before production changes.
