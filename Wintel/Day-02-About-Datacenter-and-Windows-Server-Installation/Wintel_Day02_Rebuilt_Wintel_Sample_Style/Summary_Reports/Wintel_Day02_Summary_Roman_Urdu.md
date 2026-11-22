# Wintel Day 02 — Detailed Class Summary (Roman Urdu)

## Class ka overview
Instructor ne pichhli class ke data center roles aur SLA ka revision kiya. Phir server ki definition, tower/rack/blade hardware, availability, RAID, dual PSU, remote management, server lifecycle aur home lab ke options explain kiye. Aakhir mein VMware Workstation, Rufus/UEFI aur Windows Server installation ka practical flow dekha gaya.

## Learning objectives
Server aur normal desktop ka functional farq samajhna; server downtime ka business impact explain karna; tower, rack, blade compare karna; PSU/PDU, RAID aur out-of-band management samajhna; VMware Workstation par Windows Server VM banana; Server Core aur Desktop Experience differentiate karna.

## Lecture topic-wise
**Lines 1–80:** Student introduction, data center architect aur teams ka role, requirements aur SLA. Laptop bhi services de kar server ban sakta hai.

**Lines 81–192:** Desktop purchase aur component compatibility ki discussion se tower server ka concept. Dual power supply, RAID aur patch ke baad server unreachable hone par remote management console ka use.

**Lines 193–354:** Rack mount, 42U rack, 1U/2U server, maintenance access, server replacement lifecycle, disk sanitization, aur blade hardware trade-offs.

**Lines 355–565:** Khalid ka home-lab hardware concern, refurbished vs new machine, CPU/RAM planning, VMware Workstation, ISO files aur classroom participation.

**Lines 566–866:** Windows client/server distinction, bootable USB, Rufus, UEFI, Intune ka introduction, New VM wizard, guest hardware, virtual disk aur Windows Server Core/Desktop Experience.

## Practical scenarios
1. Patching ke baad server RDP se accessible nahi: monitoring aur out-of-band console check karein.
2. RAID drive fail: correct disk identify karein aur approved rebuild monitor karein.
3. Laptop RAM limited: ek waqt mein kam VMs chalayein, host resources reserve rakhein.
4. Windows ISO boot nahi hoti: ISO attachment, firmware aur boot order verify karein.

## Key takeaways
Server build se pehle workload aur business requirements samajhna zaroori hai. Availability ek complete architecture ka result hoti hai. Har lab ke liye expensive physical server zaroori nahi. Apni actual practice, screenshots aur troubleshooting document karna chahiye.

## Interview preparation
Tower vs rack vs blade, RAID vs backup, PSU/PDU, remote management, Server Core, VM creation, Rufus aur UEFI par questions practice karein. Separate Interview_QA folder mein 35 questions dono languages mein hain.

## Suggested labs (lecture se alag)
- Host CPU/RAM/storage inventory banayein.
- VMware Workstation par Windows Server VM create karein.
- Server Core aur Desktop Experience ko alag VMs mein compare karein.
- Extra data disk add karke verify karein.
- Mock hardware incident ka runbook likhein.

## Accuracy note
Original transcript mein speech recognition ki mistakes aur mixed speaker labels hain. Exact lines Original_Source folder mein hain. English/Roman Urdu files source-based rewritten classroom adaptations hain, complete verbatim translation nahi. Technical corrections separate hain.
