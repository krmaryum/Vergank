# Wintel Day 03 — Interview Questions & Answers (Roman_Urdu)

Source: Part A and Part B lectures. Answers are technically clarified study material, not quotations from the instructor.

## Q01. What is the purpose of VMware Tools?

**Answer:** VMware Tools guest integration deta hai: display resize, time synchronization, guest status aur supported copy/paste jaise features. Har guest mein features same nahi hote.

## Q02. How do you install VMware Tools on Windows Server in Workstation?

**Answer:** VM menu mein Install VMware Tools select karein; Windows guest mein mounted CD open karke setup chalayein, components choose karein aur zarurat par restart karein.

## Q03. Why is an approved change window important before a server reboot?

**Answer:** Approved change window se downtime, approval, communication aur rollback plan clear hota hai; bina approval restart production ko impact kar sakta hai.

## Q04. What is RCA?

**Answer:** RCA yani Root Cause Analysis mein incident, root cause, impact, evidence aur future preventive actions record hote hain.

## Q05. What is Server Manager?

**Answer:** Server Manager ek Windows Server console hai jahan roles, features, alerts aur server management tasks dikhte hain.

## Q06. What does firewall.cpl open?

**Answer:** firewall.cpl se Windows Defender Firewall ka Control Panel interface khulta hai.

## Q07. Should you disable a production firewall to test connectivity?

**Answer:** Pehle firewall profiles, rules, logs aur scoped test dekhein. Production firewall complete disable karna risky hai aur approval ke baghair nahi karna chahiye.

## Q08. What is PAM?

**Answer:** PAM privileged credentials aur sessions ko approvals, audit, rotation aur least privilege ke through manage karta hai.

## Q09. What is POST?

**Answer:** POST yani Power-On Self-Test startup par firmware-led initial hardware checks ka stage hota hai, OS load hone se pehle.

## Q10. How do POST errors appear?

**Answer:** Platform ke mutabiq POST errors beep codes, diagnostic LEDs, screen messages ya out-of-band management logs mein mil sakte hain.

## Q11. What is the difference between BIOS and UEFI?

**Answer:** BIOS legacy firmware interface hai; UEFI modern firmware standard hai jo modern boot management aur Secure Boot jaise features support karta hai.

## Q12. What is CMOS/RTC battery used for?

**Answer:** CMOS/RTC battery system off hone par clock ko maintain karti hai aur kuch hardware par settings ke liye bhi use hoti hai. Weak battery se date/time galat ho sakte hain.

## Q13. What is HPE iLO?

**Answer:** HPE iLO remote console, hardware health monitoring aur power operations ke liye out-of-band management platform hai.

## Q14. What is Dell iDRAC?

**Answer:** Dell iDRAC supported Dell servers ka out-of-band remote management controller hai.

## Q15. Can iLO/iDRAC always work after a motherboard failure?

**Answer:** Nahi. Management controller ko working electronics, power aur network chahiye. Motherboard ya management failure mein access unavailable ho sakta hai.

## Q16. What is a firmware boot order?

**Answer:** Boot order woh sequence hai jisse firmware bootable disk, USB ya boot entry choose karta hai.

## Q17. What is Secure Boot?

**Answer:** Secure Boot UEFI ka feature hai jo boot-time software ki signatures/trust verify karta hai; yeh BIOS password se different hai.

## Q18. What is virtualization technology in BIOS/UEFI?

**Answer:** BIOS/UEFI mein Intel VT-x ya AMD-V jaisi processor virtualization settings enable/disable ki ja sakti hain.

## Q19. How can you check virtualization status in Windows?

**Answer:** Task Manager > Performance > CPU par Virtualization status check karein; zarurat par hypervisor compatibility bhi verify karein.

## Q20. What is Windows Boot Manager?

**Answer:** Windows Boot Manager BCD store ke mutabiq boot entry select karke Windows startup initiate karta hai.

## Q21. What is BCD?

**Answer:** BCD yani Boot Configuration Data Windows ke boot entries aur parameters store karta hai.

## Q22. What happens after Windows Boot Manager?

**Answer:** Boot Manager ke baad Windows loader, kernel, drivers aur services initialize hote hain; aakhir mein sign-in screen aati hai.

## Q23. What is the difference between restart and shutdown?

**Answer:** Restart mein OS band ho kar dobara boot hota hai; shutdown mein system power-off state mein jata hai, configuration ke mutabiq.

## Q24. Why can cluster shutdown be risky?

**Answer:** Cluster ka incorrect shutdown workloads, dependencies, shared storage ya quorum ko impact kar sakta hai; approved vendor procedure follow karein.

## Q25. How is a blade chassis different from an individual blade?

**Answer:** Blade enclosure shared power/network/management provide karta hai; ek blade off karne se poora enclosure lazmi off nahi hota.

## Q26. Why do administrators need vendor hardware support contracts?

**Answer:** Vendor support contracts diagnosis, parts replacement aur agreement-based response targets provide karte hain.

## Q27. How would you triage a server that does not POST?

**Answer:** Power, LED/beeps, management logs, recent hardware changes aur vendor documentation check karein; phir appropriate escalation karein.

## Q28. How would you triage a Windows VM with poor resolution?

**Answer:** Guest display settings, VMware Tools status, virtual video adapter aur host settings check karein.

## Q29. How do you decide VM memory allocation?

**Answer:** OS/app requirements, workload measurements, host headroom aur doosri VMs ko dekh kar RAM allocate karein; one-size-fits-all number nahi.

## Q30. Why is least privilege important to production administration?

**Answer:** Least privilege se user ko sirf required access milta hai; risk kam hota hai aur audit easy hoti hai.

## Q31. What details belong in a safe production maintenance plan?

**Answer:** Maintenance plan mein scope, impacted services, owners, approvals, backup, timing, steps, rollback, checks aur communication hoti hai.

## Q32. Can copied text from host to guest work in every secured environment?

**Answer:** Nahi. Clipboard sharing guest tools, settings aur security policies par depend karti hai; security ki wajah se disable bhi ho sakti hai.

## Q33. What is a good first answer to an interview question on Windows boot?

**Answer:** Interview mein POST, UEFI/BIOS boot selection, Boot Manager/BCD, Windows loader, kernel/drivers, services aur login ka sequence batayein.

## Q34. What should you do when an AI assistant suggests a firewall or DHCP change?

**Answer:** AI ka suggestion blindly na chalayein: verify, impact assess, safe test, approval aur rollback ke baad hi production change karein.



---

## Additional Practical Scenarios — Roman Urdu

### Scenario 1 — VM ki display chhoti reh rahi hai
**Question:** Windows Server install karne ke baad VMware Workstation window badi karne se VM display resize nahin hoti. Kya check karenge?
**Answer:** Guest OS aur Workstation compatibility check karenge; VMware Tools installed aur running hain ya nahin verify karenge; zarurat par approved reboot karenge; phir auto-fit/display settings aur remote console ki settings check karenge.

### Scenario 2 — Production server ko reboot karna hai
**Question:** Driver update reboot maang raha hai, lekin approved change window nahin. Kya karenge?
**Answer:** Bina approval reboot nahin karenge. Business impact, service owner, change approval, backup, rollback plan aur post-validation checks tayyar karenge. Emergency ho to organization ka emergency-change process follow karenge.

### Scenario 3 — Rack server par hardware alarm
**Question:** Rack server power on hota hai lekin amber LED ke saath boot nahin karta. Pehle kya steps hain?
**Answer:** LED/POST code record karenge, exact model ki vendor guide padhenge, iLO/iDRAC reachable ho to health logs dekhenge, recent changes aur power status record karenge, phir vendor support case raise karenge. Bina evidence parts indiscriminately replace nahin karenge.

### Scenario 4 — UEFI mein boot drive nahin mil rahi
**Question:** Firmware settings change hone ke baad Windows Boot Manager nahin mil raha. Kya check karenge?
**Answer:** Boot order, UEFI/legacy mode, storage controller, drive visibility, Windows Boot Manager entry, Secure Boot settings aur recent firmware changes check karenge. Recovery steps se pehle backup aur impact assess karenge.

### Scenario 5 — Hyper-V blade cluster shutdown
**Question:** Blade enclosure ko power off karna hai. Cluster problem se kaise bachenge?
**Answer:** Approved change, affected VMs aur cluster roles ki inventory, graceful workload migration/shutdown, cluster nodes drain, vendor-specific enclosure sequence, aur startup ke baad quorum/storage/services verification zaroori hai.

### Scenario 6 — Planned maintenance ka change plan
**Question:** Ek Windows Server ko patch aur reboot karna hai. Change plan mein kya shamil hoga?
**Answer:** Owner aur approvals, business impact, maintenance window, communication, pre-checks, backups, exact steps, rollback criteria, testing, evidence aur final handover.
