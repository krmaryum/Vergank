# VMware Class — Interview Questions & Answers (Roman Urdu)

**Class date:** 21 November 2026  
**Basis:** VMware-11-21-2026.txt (class transcript); questions organized by class topics.  
**Scope:** Interview preparation after the full lecture; distinct from the faithful classroom transcription.  
**Total questions:** 39

> Technical note: Yeh instructor ke word-for-word quotes nahin. Answers lecture ke scenarios par based interview preparation hain; technical corrections neeche separately mention hain.

## 01 — Foundations and Clusters

### Q1. Virtual machine ko chalane ke liye kaun se four core resources chahiye?

**Jawab:** Compute yani vCPU, RAM, networking aur storage chahiye. OS install karte waqt ISO ya doosra bootable source bhi attach karte hain. Class mein instructor ne VM creation se pehle in four resources ko identify karwaya.

### Q2. ESXi host aur datastore ki responsibility kya hoti hai?

**Jawab:** ESXi host VM ko CPU, RAM aur virtual networking services deta hai aur storage tak access bhi provide karta hai. VM ki files datastore par rehti hain jo local disk, SAN/NAS ya vSAN se backed ho sakta hai. Class mein four ESXi hosts ka cluster tha.

### Q3. vCenter mein datacenter aur cluster kya hain?

**Jawab:** Datacenter vCenter inventory ka logical container hai; zaroori nahin ke alag physical building ho. Cluster mein multiple ESXi hosts group hote hain taake HA/DRS jaisi features coordinated tareeqe se work kar sakein.

### Q4. HA, DRS aur vMotion mein kya difference hai?

**Jawab:** HA host failure ke baad affected VMs ko surviving hosts par restart karta hai. DRS placement aur load balancing manage karta hai. vMotion supported conditions mein running VM ki live migration karta hai. Host fail hone par HA ka restart live vMotion nahin hota.

### Q5. Kya HA zero downtime guarantee karta hai?

**Jawab:** Nahin. Failure detect hone, capacity check aur VM restart hone mein waqt lagta hai. Surviving host par storage aur network access bhi available hona chahiye.

### Q6. NFS, SAN aur vSAN mein kya farq hai?

**Jawab:** NFS file-sharing protocol hai jo NAS datastore ke liye use hota hai; SAN generally block LUNs expose karta hai; vSAN multiple eligible hosts ki local storage ko distributed datastore bana sakta hai. Class mein VM storage select karte waqt yeh options aaye.

## 02 — Virtual Networking

### Q7. vSphere Standard Switch (vSS) kya hota hai?

**Jawab:** vSS ESXi host ka local virtual switch hai. Is par VM port groups aur VMkernel networking connect hoti hai. Multiple hosts par alag vSS ho to names, VLANs aur physical connections ko consistent rakhna administrator ki responsibility hai.

### Q8. vSphere Distributed Switch (VDS) kya hai?

**Jawab:** VDS vCenter se centrally configure hota hai aur participating ESXi hosts par networking apply karta hai. Is se policies consistent ho sakti hain, lekin physical switches aur VLAN paths phir bhi sahi configure karne parte hain.

### Q9. Class mein VDS banane ki zaroorat kyun pesh aayi?

**Jawab:** Instructor ne scenario diya: VM host 2 se host 3 par move ho aur destination par networking ya uplink mapping different ho to connection break ho sakta hai. VDS configuration ko centralized aur consistent rakhne mein help karta hai.

### Q10. Distributed port group aur VLAN ka connection kya hai?

**Jawab:** Distributed port group VDS par VM network ka logical access point hai. Ismein VLAN aur security/team policies hoti hain. Sirf port-group name rakh dene se physical network par VLAN automatically create nahin hoti.

### Q11. VMware Lab, Cloud Lab aur Windows Lab networks kyun banaye gaye?

**Jawab:** Yeh different workloads ki logical segmentation dikhane ke examples thay. Aik VM ek port group par attach ho sakti hai, aur zaroorat par multiple vNICs se multiple networks tak connect ho sakti hai.

### Q12. VDS mein uplink kya hai?

**Jawab:** VDS ka logical uplink host ke physical NIC yani vmnic se map hota hai. Wizard mein four uplinks select karne se four actual cables nahin lag jati; NIC mapping aur physical link verify karna hota hai.

### Q13. Do active uplinks configure karne ka faida kya hai?

**Jawab:** Redundancy aur kabhi traffic distribution. Benefit teaming policy, physical switches aur actual link availability par depend karta hai. Class mein multiple uplink slots create karke selected vmnics map kiye gaye.

### Q14. VMkernel adapter aur VM port group ka difference?

**Jawab:** VMkernel (vmk) host services jaise management, vMotion ya storage ke liye IP interface hai. VM port group guest VM ke virtual NIC ko connect karta hai. Har guest-only VLAN ke liye VMkernel IP banana necessary nahin.

### Q15. Class mein kaun kaun se networks separate dikhaye gaye?

**Jawab:** Management/core, storage aur guest-VM network separate dikhaye gaye; examples mein 192.168.x.x, 172.16.x.x aur 10.x.x.x ranges thay. Real lab mein subnet, gateway, VLAN aur route settings cross-check karein.

### Q16. VDS create karne ke main steps kya hain?

**Jawab:** vCenter Networking mein datacenter select karke VDS create karein, compatible version aur uplink count choose karein, distributed port groups banayein, hosts add karein, vmnics map karein aur VLAN/connectivity test karein. Management NIC move karne se pehle rollback plan aur backup rakhein.

### Q17. VDS version ka selection kaise hota hai?

**Jawab:** Participating ESXi hosts aur vCenter ki supported versions check karke select karein. Instructor ne mixed versions ka example diya tha. Exact compatibility documentation se verify karni hoti hai.

### Q18. VM host 1 par reachable hai magar host 3 par migrate hone ke baad nahin. Kya check karein?

**Jawab:** Destination par port group, VLAN ID, trunk allowance, vmnic mapping, teaming/failover, guest IP/gateway aur security policies check karein. Source aur destination compare karein; sirf VDS hone se physical VLAN issue automatically fix nahin hota.

### Q19. Networking change se ESXi host disconnect kaise ho sakta hai?

**Jawab:** Management vmnic galat remap ho, management VLAN change ho, ya uplink policy mismatch ho to host vCenter se disconnect ho sakta hai. Console access aur stepwise rollback plan bahut important hai.

## 03 — VM Creation and Compatibility

### Q20. vCenter se VM banane ke main steps kya hain?

**Jawab:** Datacenter/cluster ya host select karein, VM name dein, compute placement aur datastore choose karein, hardware compatibility aur guest OS select karein, vCPU/RAM/disk aur port group configure karein, phir review karke finish karein.

### Q21. VM hardware compatibility pehle kyun check karni chahiye?

**Jawab:** VM ka virtual hardware version decide karta hai ke kaun se ESXi hosts usay support kar sakte hain. Newest version choose karne se older hosts par migration issue aa sakta hai. Instructor ne ESXi releases aur virtual hardware versions compare kiye.

### Q22. VM create karte waqt DRS placement kya karta hai?

**Jawab:** Configured DRS cluster suitable host recommend ya select kar sakta hai, capacity aur rules dekh kar. Manual host selection bhi possible hai. Storage, networking aur affinity rules phir bhi validate karne parte hain.

### Q23. Nested virtualization kya hoti hai?

**Jawab:** Jab hypervisor VM ke andar chal raha ho aur uske neeche aur VMs run hon. Is lab ka flow Workstation → ESXi → guest VM tha. Guest ke andar Hyper-V chalana compatibility aur CPU virtualization exposure par depend karta hai.

### Q24. CPU ya memory hot-add ka kya matlab hai?

**Jawab:** Supported guest OS aur VM settings mein vCPU/RAM increase power-off ke baghair ho sakta hai. Yeh har VM ke liye mandatory nahin aur har combination mein supported bhi nahin. Instructor ne wizard mein options enable kiye.

### Q25. Kya aik VM do alag port groups se connect ho sakti hai?

**Jawab:** Haan, multiple virtual NICs de sakte hain: ek VMware Lab aur ek Cloud Lab. Guest mein IP/routing carefully configure karein taake security isolation accidentally bypass na ho.

## 04 — Storage and Disk Provisioning

### Q26. Thin provisioning ki example dein.

**Jawab:** Guest ko 100 GB disk nazar aa sakti hai magar datastore par initially kam physical space consume ho. Data likhne ke saath allocation grow hoti hai. Is liye datastore free capacity aur alerts monitor karein.

### Q27. Thick lazy-zeroed aur eager-zeroed mein kya farq hai?

**Jawab:** Dono disk capacity up front allocate karte hain. Lazy-zeroed blocks ko first write par zero kar sakta hai; eager-zeroed disk creation par zeroing karta hai. Exact features aur availability environment par depend karti hain.

### Q28. Thin ke bajaye thick kab choose karna chahiye?

**Jawab:** Thin capacity flexibility deta hai magar monitoring zaroori hai. Thick allocation/reservation aur kuch workload policies ke liye preferred ho sakta hai. Selection datastore type, capacity aur operational standards par depend karegi.

### Q29. Existing VM mein nayi disk kaise add karenge?

**Jawab:** VM settings mein Add New Hard Disk select karein, capacity/datastore/provisioning set karein, phir guest OS ke andar rescan aur zaroorat ke mutabiq initialize/partition/format karein. Existing data disk ko galti se format na karein.

### Q30. RDM kya hota hai?

**Jawab:** Raw Device Mapping VM ko raw block LUN tak access deta hai mapping file ke zariye. Yeh normal VMDK aur thin/thick provisioning se alag concept hai. Use karne se pehle workload requirement aur support check karein.

### Q31. Storage vMotion kya karta hai?

**Jawab:** Storage vMotion supported situation mein VM ki disks ko doosre datastore par move karta hai, aksar VM on rehte hue. Compute vMotion VM ka running execution host-to-host migrate karta hai; dono ke prerequisites different hain.

### Q32. Kya thin disk thick aur thick disk thin mein convert ho sakti hai?

**Jawab:** Kuch supported migration, cloning ya disk operations mein conversion possible hoti hai. Instructor ne storage change ke waqt conversion discuss ki. Har method mein zero downtime assume na karein; exact steps aur free space verify karein.

### Q33. ESXi host par datastore missing ho to pehle kya check karein?

**Jawab:** Storage controller/adapter, rescan, devices, paths, LUN presentation, VMFS mount, connectivity aur logs check karein. Nested Workstation lab mein virtual disk attached hai ya nahin verify karein. Host reset ko first fix na banayein.

### Q34. Reset System Configuration risky kyun hai?

**Jawab:** Yeh ESXi host ki configurations remove kar deta hai; network/storage settings bhi affect ho sakti hain. Instructor ne isay datastore issue ke context mein dikhaya, magar production mein yeh disruptive action hai aur prior backup, approval, recovery plan chahiye.

## 05 — Identity and Operations

### Q35. vCenter ko Active Directory se integrate kyun karte hain?

**Jawab:** Taake centrally managed AD identities vCenter mein authenticate kar saken aur unko required vSphere permissions mil sakein. Har AD user automatically administrator nahin banta; role assignment alag hoti hai.

### Q36. AD identity integration se pehle kya verify karein?

**Jawab:** Domain DNS, DC reachability, time synchronization, required TLS/certificates, proper account permissions aur supported identity-source method check karein. Lecture mein VCPLAB.com lab domain use hua; credentials GitHub par share na karein.

### Q37. vCenter aur AD authentication mein DNS kyun important hai?

**Jawab:** Identity services ko domain controllers aur endpoints resolve karne ke liye sahi DNS chahiye. Wrong resolver ya DNS records se login fail ho sakta hai, chahe ping by IP theek chal raha ho.

### Q38. VDS aur VM deployment lab ka documentation evidence kya ho?

**Jawab:** Network topology, vmnic-uplink mapping, VLAN IDs, port groups, IP/subnets, VM placement, datastore/provisioning, connectivity tests aur vCenter task screenshots capture karein. Rollback steps likhein aur passwords/tokens hide karein.

### Q39. Interview mein is VMware class ko practical experience ke taur par kaise explain karein?

**Jawab:** Scenario batayein: vCenter cluster mein four ESXi hosts, separate management/storage/VM networks, VDS aur distributed port groups, uplink mapping, phir VM creation aur disk provisioning. Network migration risk explain karein, aur end par network/storage/AD verification steps batayein.

---

## Technical clarification (original transcript se alag)

- **vCPU** ka matlab virtual CPU hai, “vSphere CPU” nahin.
- **HA** failed host ki VMs ko restart karta hai; failed host se live migration nahin hoti.
- **VMkernel** host services ke liye hota hai; guest port group ke liye alag vmk IP mandatory nahin.
- **VDS** physical VLAN trunk aur vmnic mapping ki galti ko khud se fix nahin karta.
- **Thin/thick** disk allocation models hain; **RDM** alag storage mapping concept hai.
- **Reset System Configuration** ko datastore issue ka first troubleshooting step na banayein.
- **Compatibility** apni actual ESXi/vCenter version se check karein.
- **AD integration** ka supported method version par depend karta hai; credentials GitHub par na daalein.

### Source

Original lecture: `VMware-11-21-2026.txt` (included unchanged in the ZIP).
