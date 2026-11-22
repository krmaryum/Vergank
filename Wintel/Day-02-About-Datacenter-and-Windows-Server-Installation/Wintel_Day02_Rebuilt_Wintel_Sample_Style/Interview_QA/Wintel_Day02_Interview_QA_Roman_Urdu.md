# Wintel Day 02 — 35 Interview Questions & Answers (Roman Urdu)

Based on the Day 02 class themes; answers incorporate separately identified best-practice clarifications where needed. Interview preparation is **additional material**, not words attributed to the instructor.

## Q01. Kya laptop ya desktop server ban sakta hai?

**Answer:** Ji haan. Server woh system hai jo services deta hai. Desktop par web, file ya print service chal sakti hai, lekin production reliability ke liye dedicated server hardware behtar ho sakta hai.

## Q02. Server downtime se business ko kya nuqsan hota hai?

**Answer:** Banking ya website ki service band ho jaye to customer ka kaam ruk sakta hai, revenue aur trust affect hota hai.

## Q03. Tower aur rack server mein kya farq hai?

**Answer:** Tower ka chassis freestanding hota hai; rack server standard rack mein mount hota hai. Dono ki performance exact model aur configuration par depend karti hai.

## Q04. Redundant PSU kya hota hai?

**Answer:** Dual PSU aur sahi independent power feeds ke saath ek power source fail hone par doosra supply continue kar sakta hai.

## Q05. RAID kya hai aur kya har RAID disk failure se bachata hai?

**Answer:** RAID disks ko combine karta hai. RAID 1 jaise levels redundancy dete hain, lekin RAID 0 nahi deta. RAID backup ka replacement nahi.

## Q06. RAID disk fail ho jaye to pehle kya check karenge?

**Answer:** Array alerts, failed disk ki exact identification, backups, hot-swap support, approved replacement aur rebuild status verify karenge.

## Q07. Out-of-band management kya hai?

**Answer:** Dedicated management controller se OS unavailable honay par bhi authorized admin hardware health, remote console aur power state check kar sakta hai.

## Q08. Patch ke baad RDP nahi aa raha; kya karenge?

**Answer:** Monitoring, ping/network path, remote hardware console, patch/boot status aur alerts check karunga. Hard reset sirf evidence aur approval ke saath.

## Q09. PSU aur PDU mein farq kya hai?

**Answer:** PSU server ke andar power convert/regulate karta hai. PDU rack mein multiple devices ko power distribute karta hai.

## Q10. Rack unit (U) kya hota hai?

**Answer:** 1U rack height ka standard unit 1.75 inches hai. 2U server do units height occupy karta hai.

## Q11. Kya 42U rack mein hamesha 42 servers aate hain?

**Answer:** Nahi. Servers 1U, 2U ya zyada ho sakte hain aur networking/cabling/power equipment bhi space leta hai.

## Q12. Kya har rack server ke beech 1U gap zaroori hai?

**Answer:** Nahi, universal rule nahi. Vendor ki cooling aur rack-mount guidance follow karein; khali spaces mein blanking panels ki zaroorat ho sakti hai.

## Q13. Small business mein tower server kyun useful hota hai?

**Answer:** File, print, directory aur applications chala sakta hai; full rack ki requirement nahi, agar capacity aur availability needs suit karti hon.

## Q14. Server choose karte waqt kya dekhenge?

**Answer:** Workload, CPU/RAM, storage, NIC, redundancy, remote management, warranty, lifecycle, support aur total cost.

## Q15. Blade server kya hota hai?

**Answer:** Blade ek modular compute unit hai jo shared chassis mein install hota hai aur power/cooling/management jaise components share kar sakta hai.

## Q16. Shared chassis failure domain ka matlab?

**Answer:** Shared chassis ka component fail ho to multiple blades affect ho sakte hain; redundancy aur recovery planning zaroori hai.

## Q17. Server lifecycle management kya hai?

**Answer:** Procurement se deploy, monitor, patch, refresh, migrate aur secure retirement tak poori planning.

## Q18. Secure decommissioning kaise hoti hai?

**Answer:** Service se remove, access revoke, disk secure erase/destroy aur disposal ka record policy ke mutabiq rakhte hain.

## Q19. Sensitive disk ke liye sirf format kyun kaafi nahi?

**Answer:** Formatting ke baad data recover ho sakta hai; approved secure erase ya destruction method use karein.

## Q20. Physical server ke baghair Windows lab ban sakti hai?

**Answer:** Haan. Sufficient RAM/CPU wala host VMware Workstation par Windows Server VMs chala sakta hai.

## Q21. Host aur guest kya hotay hain?

**Answer:** Host physical computer/hypervisor environment hai, aur guest VM ke andar chalne wala operating system hai.

## Q22. VM ko RAM carefully kyun deni chahiye?

**Answer:** VM host ki real RAM use karti hai; zyada allocation se host aur guest slow ho sakte hain.

## Q23. Windows Server bare metal kab install karenge?

**Answer:** Jab workload ko direct hardware access ya specific performance/architecture chahiye ho; labs mein VM flexible rehti hai.

## Q24. ISO file kis liye use hoti hai?

**Answer:** ISO installation media hoti hai jo VM mein mount ho sakti hai ya bootable USB prepare karne mein use hoti hai.

## Q25. Rufus kis liye use hota hai?

**Answer:** Rufus ISO se bootable USB banata hai; correct USB select karein kyunke process data erase kar sakta hai.

## Q26. UEFI kya hai?

**Answer:** UEFI modern firmware hai jo boot process start karti hai. USB aur partition settings boot mode se match honi chahiye.

## Q27. New VM wizard mein kya select karte hain?

**Answer:** ISO, OS version, VM name/location, vCPU, RAM, virtual disk aur network options.

## Q28. OS aur data disks alag kyun banate hain?

**Answer:** Management, backup aur recovery planning easier ho sakti hai, lekin alag disks automatically redundancy nahi detin.

## Q29. Windows Server Core kya hai?

**Answer:** Server Core minimal UI wala installation option hai; PowerShell aur remote tools se manage kiya jata hai.

## Q30. Desktop Experience aur Server Core mein kya farq hai?

**Answer:** Desktop Experience full GUI deta hai; Core minimal local GUI aur command/remote management use karta hai.

## Q31. VM ISO se boot nahi hoti; kya check karenge?

**Answer:** ISO valid hai? CD/DVD connected hai? Boot order, firmware aur compatibility sahi hai? Pehle non-destructive checks karenge.

## Q32. Microsoft Intune kya hai?

**Answer:** Endpoint management service hai jo device policies, apps aur updates manage kar sakti hai; AD DS se alag service hai.

## Q33. Interview mein apna home lab kaise explain karenge?

**Answer:** Host specs, VMware software, VM roles, networking, screenshots, verification aur apni troubleshooting honestly describe karenge.

## Q34. Server lab ke baad kya document karna chahiye?

**Answer:** Objective, requirements, VM specs, OS edition, steps, screenshots, verification, issues aur cleanup note.

## Q35. Hard reboot se pehle kya karna chahiye?

**Answer:** Updates aur critical work check karein, impact samjhein, approval/runbook follow karein aur graceful option pehle use karein.

