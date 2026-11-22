# Wintel Lecture — Interview Questions & Answers (Roman Urdu)

**Coverage:** Wintel lecture ke Parts 1–3, original transcript ki taqreeban lines 1–496. Baqi 497–835 lines is package mein cover nahin hain.

**Istemaal:** Har jawab ko samajh kar interview mein 45–90 seconds mein bolne ki practice karein. Instructor ki class examples ko example samjhein; jahan professional technical clarification di hai woh instructor ka word-for-word quote nahin hai.

**Source:** `wintel.txt` aur existing Parts 1–3 bilingual notes. Yeh interview practice ke liye naye Q&A hain, full transcript nahin.


## Wintel aur Server Fundamentals

### Q1. What does Wintel mean in an enterprise infrastructure context?

**Jawab (Roman Urdu):** Wintel ka matlab aam tor par Windows aur Intel-compatible x86 platform ka combination hai. Lecture mein Windows Server software aur server hardware ke connection ko samjhane ke liye yeh term use hui; aaj AMD-based systems bhi commonly use hotay hain.

### Q2. Does a server have to be dedicated server hardware?

**Jawab (Roman Urdu):** Nahin. Server woh system hai jo clients ko service provide karta hai. Instructor ne laptop/desktop se printer share karne aur applications ki files dene ki examples di. Enterprise mein dedicated hardware performance, reliability aur management ki wajah se use hota hai.

### Q3. How does the cybercafé print-server example work?

**Jawab (Roman Urdu):** Cybercafé mein printer aik computer ke saath connected hai. Network par baqi computers us shared printer ko print jobs bhejte hain. Is example se server-client relationship samajh aata hai, baghair dedicated server hardware ke.

### Q4. What is the purpose of a file-transfer server in the instructor’s example?

**Jawab (Roman Urdu):** Administrator Chrome, Firefox, Adobe Reader waghera ke installers aik dafa download karke central system par rakhta hai. Doosray network computers wahin se files lete hain. Is se repeated downloads kam hoti hain aur internet down ho to bhi files mil sakti hain.

### Q5. What does FTP stand for, and how is it different from SFTP?

**Jawab (Roman Urdu):** FTP ka full form File Transfer Protocol hai, aur default mein encryption nahin hoti. SFTP ka matlab SSH File Transfer Protocol hai, jo encrypted SSH connection use karta hai. Upload ya download hone se protocol FTP ya SFTP decide nahin hota.

### Q6. What is the difference between HPE, Dell, Lenovo, Intel, and AMD in a server discussion?

**Jawab (Roman Urdu):** HPE, Dell aur Lenovo branded servers aur support solutions provide karte hain; Intel aur AMD bohat se servers mein processors banate hain. Lecture ka point yeh tha ke branded server vendor aur processor maker ki responsibilities alag hoti hain.


## Enterprise Teams aur Identity Services

### Q7. Why should a Wintel engineer understand multiple IT teams?

**Jawab (Roman Urdu):** Real deployment mein physical servers, storage, virtualization, operating system, networking aur security teams hoti hain. Instructor ne students ko alag roles dekar samjhaya ke architect teams aur dependencies ko coordinate karta hai.

### Q8. What were the team roles in the class scenario?

**Jawab (Roman Urdu):** Class ki example mein Nadeem storage, Khalid virtualization, Sarfraz physical servers, Anil operating systems aur instructor data-center architect ke role mein thay. Yeh learning scenario tha, permanent job duties ka claim nahin.

### Q9. What does identity and access management accomplish?

**Jawab (Roman Urdu):** IAM ka maqsad users ki identity, authentication aur suitable permissions manage karna hai. Instructor ki company example mein Active Directory Domain Services centralized user aur access management ke liye use hoti hai.

### Q10. Why might an internal company need AD DS, DNS, and DHCP?

**Jawab (Roman Urdu):** AD DS domain users aur identities manage karta hai; DNS names ko resolve karta hai; DHCP clients ko IP aur network settings automatically de sakta hai. Lecture mein yeh essential enterprise services ke taur par aaye.

### Q11. What is the role of HTTPS and a certificate authority?

**Jawab (Roman Urdu):** HTTPS, TLS ke zariye web connection protect karta hai. Certificate Authority certificates issue/sign karti hai jin se client server identity par trust kar sakta hai. Instructor ne CA ko company infrastructure ka hissa bataya; public site ke liye visitors ke trusted certificates chahiye hotay hain.

### Q12. What does “resource” mean in an IT service project?

**Jawab (Roman Urdu):** Class mein resource ka matlab log, systems, capacity aur woh assets hain jo project complete karne ke liye chahiye hotay hain. Architect ko resources, timing aur cost plan karni hoti hai.


## Production Server Builds aur SLA

### Q13. Why is server build not the same as operating-system installation?

**Jawab (Roman Urdu):** Enterprise server build mein hardware preparation, remote management, RAID/storage, firmware updates, OS deployment, network configuration, monitoring, security, patching aur verification shamil hain. Windows install karna sirf aik stage hai.

### Q14. What is iLO and why would an administrator use it?

**Jawab (Roman Urdu):** HPE iLO out-of-band management interface hai, jis se supported server ko remotely monitor/control kiya ja sakta hai, jaise console aur power operations. Lecture ke server-build checklist mein iLO shamil hai.

### Q15. What is RAID and where does it fit in the build process?

**Jawab (Roman Urdu):** RAID physical disks ko logical storage arrangement mein combine karta hai, redundancy aur/ya performance ke liye, RAID level ke mutabiq. Instructor ke build flow mein RAID configuration OS installation se pehle aati hai.

### Q16. Why are firmware upgrades part of a server build?

**Jawab (Roman Urdu):** Firmware BIOS/UEFI, controllers aur adapters jaise components ko control karta hai. Approved updates compatibility, reliability aur security issues solve kar sakti hain. Production mein vendor compatibility aur change process follow karna chahiye.

### Q17. What does an eight-hour server-build SLA mean?

**Jawab (Roman Urdu):** Instructor ki example mein 8-hour SLA ka matlab task complete karne ki service-level window hai. Is mein coordination, interruptions, reboot aur buffer time hota hai; sirf Windows installation 8 ghantay nahin leti. Actual SLA har company mein different ho sakta hai.

### Q18. Why can a production server reboot take longer than a desktop reboot?

**Jawab (Roman Urdu):** Enterprise server reboot mein firmware checks, controller initialization, hardware tests aur post-patch processing ho sakti hai. Lecture mein patch ke baad kuch reboots 10–20 minutes lene ki example di gayi, is liye planning zaroori hai.

### Q19. What should you do if competing incidents put your build SLA at risk?

**Jawab (Roman Urdu):** Agar multiple tasks ki wajah se SLA risk mein ho, jaldi communicate karein, status document karein aur clear handover/escalation karein taake doosra teammate kaam continue kar sakay. Instructor ne isi coordination par zor diya.


## Enterprise Project aur Capacity Planning

### Q20. What questions should an architect ask after a customer requests 1,500 servers?

**Jawab (Roman Urdu):** Agar customer 1,500 servers maangay, architect workload, physical/virtual split, cloud use, sizing, storage, network, security, availability, DR, location, budget aur timeline clear kare. Class mein server count se poori architecture planning tak baat pohanchi.

### Q21. How did the instructor split the 1,500-server example?

**Jawab (Roman Urdu):** Class ki example mein takreeban 200 physical, 800 virtual aur 500 cloud servers ka split diya gaya—total 1,500. Yeh sirf illustrative example hai, har project ke liye fixed ratio nahin.

### Q22. Does a request for 1,500 servers mean buying 1,500 physical machines?

**Jawab (Roman Urdu):** Nahin. Bohat se server instances virtual machines ki shakal mein kam physical hosts par chal saktay hain, aur kuch cloud par. Host count capacity, availability, performance aur licensing par depend karta hai.

### Q23. Why should server administrators understand the whole data center?

**Jawab (Roman Urdu):** Server power, cooling, racks, networking, storage, access control, monitoring aur support par depend karta hai. Puri data center understanding se incident diagnosis aur teams ke saath recovery coordination behtar hoti hai.

### Q24. What is the difference between on-premises, virtualized, and cloud deployments?

**Jawab (Roman Urdu):** On-premises batata hai physical site kahan aur kis ke control mein hai; virtualization se VMs chalti hain; cloud service delivery/operating model hai. Yeh categories overlap kar sakti hain: on-prem aur cloud dono par VMs chal sakti hain.

### Q25. What is the relevance of PMP, PRINCE2, and ITIL in the lecture?

**Jawab (Roman Urdu):** Instructor ne PMP, PRINCE2 aur ITIL ko project acquire, deliver aur manage karne ke context mein mention kiya. PMP aur PRINCE2 project management se, ITIL IT service management se related hain. Inka purpose sirf marketing ya transparency tak limited nahin.


## Colocation, Support aur Operations

### Q26. What is data-center colocation?

**Jawab (Roman Urdu):** Colocation mein company apna ya leased hardware third-party facility mein rakhti hai; facility racks, power, cooling, connectivity aur physical infrastructure deti hai. Lecture mein Noida aur overseas data centers ki examples aayi hain.

### Q27. What should you check before choosing a colocation provider?

**Jawab (Roman Urdu):** Colocation provider choose karte waqt uptime, redundant power/cooling, connectivity, physical security, remote hands, access, support response, location risks, compliance aur total cost check karein. Instructor ne setup dekhne aur verify karne par zor diya.

### Q28. Can every engineer enter a third-party data center?

**Jawab (Roman Urdu):** Har engineer ko data center mein entry nahin milti. Aksar approved personnel ko identity verification aur provider process ke baad access milta hai. Lecture mein authorized visits aur supervised vendor work discuss hua.

### Q29. How are physical faults addressed when admins work remotely?

**Jawab (Roman Urdu):** Remote admin pehle evidence collect karta hai, OEM ya facility support case raise karta hai, remote-hands/team se coordinate karta hai, approved access arrange karta hai aur repair verify karta hai. Yeh lecture ki remote operations examples se related hai.

### Q30. Why are hardware support contracts important?

**Jawab (Roman Urdu):** Enterprise hardware fail ho sakta hai. Support contracts replacement parts, vendor engineers aur response arrangement define karte hain. Instructor ne 5-year support ki example di; actual duration purchasing contract par depend karti hai.

### Q31. Why might staffing decrease after a deployment goes live?

**Jawab (Roman Urdu):** Build/migration phase mein temporary team badi ho sakti hai; go-live ke baad monitoring aur support processes stable hon to routine operations mein kam staff lag sakta hai. Lecture mein contract staffing aur 24×7 coverage discuss hui.


## Disaster Recovery aur Interview Scenarios

### Q32. What is the difference between a primary site and a DR site?

**Jawab (Roman Urdu):** Primary site par normally production workloads chalti hain. DR site par alternate resources aur recovery procedures hotay hain, taake primary fail ho to critical services restore/continue ki ja sakein. Instructor ne alag locations ki example di.

### Q33. What is RTO?

**Jawab (Roman Urdu):** RTO, Recovery Time Objective, woh target maximum duration hai jis ke andar service restore karni hoti hai. Misal: 4-hour RTO ka matlab service ko chaar ghanton ke andar wapas lana target hai.

### Q34. What is RPO?

**Jawab (Roman Urdu):** RPO, Recovery Point Objective, time ke hisaab se acceptable data-loss window hai. Misal: 15-minute RPO mein design ka target hota hai ke taqreeban 15 minutes se zyada recent changes lose na hon.

### Q35. What is the difference between backup, high availability, and disaster recovery?

**Jawab (Roman Urdu):** Backup data ki recoverable copy hai; High Availability component failure se downtime kam karti hai; DR bade service/site failure ke baad recovery deta hai. Yeh aik doosray ke alternatives nahin, complementary controls hain.

### Q36. Why should an organization conduct DR drills?

**Jawab (Roman Urdu):** DR plan test na ho to actual emergency mein fail ho sakta hai. DR drills recovery steps, dependencies, communication, RTO/RPO targets aur team readiness validate karti hain. Lecture mein DR drills ko planning ka hissa bataya gaya.

### Q37. How would you answer an interview question: “Tell me your approach to a new data-center project”?

**Jawab (Roman Urdu):** Pehle business aur application requirements clear karunga. Phir capacity, physical/virtual/cloud split, site/colocation, network/storage/security, build ownership, SLAs aur RTO/RPO plan karunga. Us ke baad phased deployment, testing, documentation aur operations handover karunga. Yeh instructor scenario ki bunyaad par interview sample answer hai.


## Additional interview practice (naye exercises)

1. Server build ke acceptance checklist ko explain karein.
2. Class ki *illustrative* 1,500-server architecture ka simple diagram banayein.
3. ESXi ya Windows server unreachable ho to pehli 5 checks batayein.
4. DR runbook banayein: owners, prerequisites, communication steps aur recovery verification.

*Yeh additional study suggestions hain, instructor ke direct classroom sawal nahin.*
