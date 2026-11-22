# Wintel Day 03 — Part A: Roman Urdu Classroom Translation

## Section 1 — Pichhli classes ka recap aur lab hypervisor ka selection

**Instructor (A:1–3):** Companies kya karti hain? Hum aksar sunte hain ke kisi company mein hazaron servers hain. Itne servers kyun hote hain? Company ki requirements kya hoti hain? Projects kya hote hain, projects par kaise kaam hota hai, aur tickets kya hoti hain? Jab aap is session ko detail mein dekhenge to ye saari cheezen samajh aayengi. Aap pehle applications par technical support dete rahe honge; yahan hum servers aur infrastructure ke perspective se baat kar rahe hain.

**Instructor (A:4–5):** Aap SLA, tickets, aur P1, P2, P3 tickets ke concepts se pehle hi waqif hain, theek hai? Day 01 mein humne ye cheezen discuss ki thin.

**Instructor (A:6–9):** Day 02 mein humne operating system, server ke tasks, aur data center ke components samjhe: routing, switching, network devices, storage, power setup, aur servers ki different types. Humne ye bhi dekha ke Windows Server ko apne laptop ya desktop ke lab mein kaise deploy kar sakte hain, kyun ke har student ke liye naya physical server khareedna mumkin nahin hota.

**Instructor (A:10–12):** Kal humne Windows Server 2022 deploy kiya tha. Windows Server 2025 bhi install kar sakte hain; installation ka general process milta-julta hai. Agli class mein 2025 bhi lab mein deploy karenge. Pehle main kal wala server power on karta hoon. Hamare lab mein VMware Workstation use ho raha hai.

**Instructor (A:13–18):** Hum Microsoft Hyper-V abhi kyun use nahin kar rahe? Is liye ke abhi Hyper-V nahin padha. Agar shuru mein hi Hyper-V ka role aur uski terminology introduce kar doon to kuch students confuse ho sakte hain. Hum aage chal kar Hyper-V ka role install aur configure karna bhi seekhenge. Filhal VMware Workstation use karenge. Ye Microsoft ki application nahin hai; third-party product hai, aur hum jo edition use kar rahe hain uske liye alag se fee nahin deni.

**Student (A:19):** Sir, VirtualBox aur VMware mein kya farq hai?

**Instructor (A:19–28):** VirtualBox Oracle company ka product hai. VMware mein pehle VMware Player aur VMware Workstation alag products the. Workstation Pro paid bhi raha hai. Ab hum naya version use kar rahe hain, jise instructor pehle 26H2 aur phir 26H1 kehte hain. Mera approach ye hai ke har haal mein bilkul latest version par na jaaya jaye; kabhi kabhi ek tested aur reliable version behtar hota hai taake naye bugs se bacha ja sake.

**Instructor (A:29–34):** VMware Workstation mein snapshots aur advanced virtual networking jaise features hain. Meri YouTube playlist mein iska networking section bhi hai. Mere experience mein ye training ke liye kaafi feature-rich aur user-friendly hai. Hyper-V ke muqablay mein asaan hone ki baat instructor ki personal preference hai.

## Section 2 — Windows Server install karne ke baad VMware Tools kyun chahiye?

**Instructor (A:35–38):** Kal humne VMware Workstation ke andar Windows Server install kiya tha. Pehli baar login karte waqt graphics ya display resolution utna achha nahin lag sakta. Server OS ka focus Windows 10 ya Windows 11 jaisi desktop appearance nahin hota. Iske ilawa virtual machine mein abhi VMware Tools ke integration components aur drivers installed nahin hain.

**Instructor (A:39–44):** VMware Workstation ek Type 2 hypervisor hai. Production mein Type 1 hypervisors bhi use hote hain, jin par hamari doosri VMware class mein practice hoti hai. Type 1 aur Type 2 ka farq hum Hyper-V chapter mein detail se discuss karenge. VMware ki Windows guest VM ke liye VMware Tools install karna recommended hai.

**Instructor (A:45–47):** Is VM ko full-screen karne par left aur right side black space nazar aa rahi hai. Start button bhi chhoti si guest screen ke andar dikh raha hai. Yani guest display hamari poori window ke size ke mutabiq resize nahin ho raha.

**Instructor (A:48–49):** Farz karein host computer ke desktop par ek file hai aur aap use virtual machine mein copy karna chahte hain. VMware Tools ki integration settings sahi hon to copy-paste jaisi facilities mil sakti hain. Abhi demonstration mein ye option is liye available nahin kyun ke Tools installed nahin hain.

**Instructor (A:50–56):** Aaj ka pehla practical VMware Tools install karna hai. Windows guest install hone ke baad Tools check karein. Neeche notification aa sakti hai ke Tools installed nahin. Aap notification par click kar sakte hain, VM tab par right-click kar sakte hain, ya upar **VM** menu mein **Install VMware Tools** select kar sakte hain.

**Instructor (A:57–62):** Is option ko choose karne par VMware Tools ka installer virtual ISO ki tarah guest ke saath attach ho jata hai. Windows guest ke andar wapas aayein. AutoPlay popup aa sakta hai; warna **This PC** mein virtual DVD khol kar setup run karein. Zarurat ho to setup ko **Run as administrator** karein.

**Instructor (A:63–68):** Installer wizard mein main **Typical** ki bajaye **Complete** select kar raha hoon taake is demonstration ke liye tamam components install hon. Phir Next aur Install click karta hoon. Kuch waqt baad restart ka message aayega.

**Instructor (A:69–77):** Yahan enterprise change management ka ek important point hai. Naye server build ke liye company 4, 6 ya 8 ghanton ki approved maintenance window de sakti hai. Us window mein planned reboot karna allowed ho sakta hai. Lekin bina approval production server reboot karne se escalation aa sakti hai. Phir RCA yani Root Cause Analysis mein batana pad sakta hai ke incident kyun hua aur future mein kya preventive action lenge. Hamare lab mein ye planned activity hai, is liye ab reboot kar sakte hain.

**Instructor (A:78):** Restart ke baad VMware Workstation ki window ko chhota ya bada karne par VM ka display bhi behtar tareeqe se adjust ho jayega.


---

# Day 03 Part A — VMware Tools verification, performance and student questions

**Original-source reference:** A:79–128.

**Instructor (A:79–83):** Reboot ke baad display ka result dekhiye. Ab screen poori fit ho rahi hai, aur jab main VMware Workstation ki window ko chhota karta hoon to guest OS apna resolution adjust kar raha hai. Student se poochta hoon ke pehle virtualization labs banaye hain? Jawab aata hai ke Linux aur Windows ki VMs VirtualBox mein banayi hain, VMware mein nahin. Main kehta hoon ke jis tool se familiarity hoti hai, insaan use hi sabse convenient samajhta hai. Lekin Workstation mein extra integration aur networking options hain.

**Student (A:84):** Sir, kuch log kehte hain VMware heavy hai aur VirtualBox halka. Yeh baat kya hai?

**Instructor (A:85–92):** Main samjhata hoon ke zyada features hone ki wajah se program ki services aur resource utilization alag ho sakti hai. Task Manager se CPU aur RAM check ki ja sakti hai. Purane Windows XP aur Windows Server 2003 ke din yaad karein: us waqt 64 MB, 128 MB, 256 MB, ya 512 MB RAM ki baat hoti thi. Aaj hardware aur applications ki requirements bohat badh chuki hain. Mobile phones mein bhi kai gigabytes RAM aam hai. Is se example milta hai ke software functionality ka infrastructure par asar hota hai.

**Instructor (A:93–103):** Ab Windows Server ke Core aur Desktop Experience options ki baat karte hain. Installation ke bare minimum aur practical RAM allocation ko ek na samjhein. Instructor ke classroom example mein 1–2 GB minimum-style values aur 4–8 GB ka practical starting range aata hai, lekin actual need installed roles aur workloads par depend karegi. Aapki host machine mein 8–16 GB RAM aur SSD ho to chhoti lab manageable ho sakti hai. Agar HDD slow ho, CPU constrained ho, ya multiple VMs chal rahi hon, to lag/latency ka impression aa sakta hai. Instructor apni tower machine aur purane refurbished laptop ke examples dete hain.

**Student (A:109–110):** Sir, pichli baar VMware use kiya to problem thi; is baar aapke installer se nahin aayi. Kya pehle mujhe use karna nahin aata tha?

**Instructor (A:111–128):** Nahin, aisa zaroori nahin. Version compatibility, operating system, hardware support aur updates farq daal sakte hain. Kabhi user jis product ko pasand karta hai uski chhoti problems bhi accept kar leta hai. Motorbike change karne ki misaal deta hoon: nayi bike aapki apni choice ho to uski learning curve bhi accept karte hain. Workstation ke purane 15/16 releases aur naye versions ki functionality alag ho sakti hai. Ab jab server mein login karta hoon, screen resize ho rahi hai; Ctrl+Alt se host par wapas aa sakte hain aur guest ke andar tools ka fayda saamne hai.


---

# Day 03 Part A — Server Manager, auto-start and Internet Explorer

**Original-source reference:** A:129–153.

**Instructor (A:129–136):** VMware Tools ke baad host aur guest ke darmiyan kuch integration features available ho gaye hain. Ab Windows Server ki administrative side dekhiye. Login par Server Manager ki window aam tor par open hoti hai. Hum is se server ki configuration aur management areas mein ja sakte hain. Yeh sirf welcome screen nahin; roles aur system health ka entry point hai.

**Instructor (A:137–147):** Server Manager ke andar server status aur alerts check kar sakte hain. Agar aap baar-baar console ka automatic launch nahin chahte to relevant setting se 'Do not start Server Manager automatically at logon' jaisa option configure kar sakte hain. Is se application uninstall nahin hoti—sirf logon par uska automatic launch band hota hai. Jab zaroorat ho Start menu ya management shortcut se phir khol sakte hain.

**Instructor (A:148–153):** Ek chhoti operational habit bhi samjho: window ko sirf minimize kar dena aur uska auto-start behavior change karna alag cheezen hain. Aap jis server par kaam karte hain, uski background management consoles ko samajh kar handle karein. Ab browser aur legacy software ke security implications par baat karte hain; Internet Explorer purana ho chuka hai aur enterprise vulnerability scans usay flag kar sakte hain.


---

# Day 03 Part A — Vulnerability scanning, Defender and centralized antivirus

**Original-source reference:** A:154–194.

**Instructor (A:154–161):** Companies security audits aur vulnerability scans karti hain. Agar server par outdated Internet Explorer ya koi vulnerable component ho to report mein alert aa sakta hai. Instructor kehte hain ke ek PowerShell script se relevant old components ke status ko check ya manage karne ka example mil sakta hai. Actual script recording mein text ki shakal mein available nahin, is liye yahan main koi command invent nahin kar raha. Production par script run karne se pehle approval aur compatibility verify karni hogi.

**Instructor (A:162–172):** Naya Windows Server install ho to kya alag antivirus lazmi hai? Instructor built-in Microsoft Defender ki taraf dhyan dilate hain. Server ki existing protection check karein. Iska matlab nahin ke har organization third-party security product bilkul use nahin karti: policies, licensing, threat detection aur managed SOC architecture ke mutabiq selection hota hai. Instructor ke demo mein ek infected file detect hone aur scan report ka general behavior discuss hota hai.

**Instructor (A:173–181):** Kuch companies SentinelOne, Norton ya doosre vendors ke endpoint security agents deploy karti hain. Enterprise mein in products ka management aksar central web portal se hota hai. Is portal mein machine ki onboarding, scan status, policy, alert aur uninstallation authorization ka control ho sakta hai. Local administrator har managed agent ko seedha uninstall nahin kar sakta, kyun ke tamper protection aur central control hota hai.

**Instructor (A:182–194):** Agar team ko local policy ka access diya gaya ho to woh individual scan ya protection options bhi review kar sakti hai. Company mobile phones aur remote endpoints ko bhi cloud management se secure kar sakti hai, jahan subscription aur management authority ka sawal aata hai. Lecture ka lesson hai: 'server install ho gaya' security configuration complete hone ka proof nahin; built-in protection, central policy, vulnerability reporting aur organizational standard check karna hota hai.


---

# Day 03 Part A — Windows Defender Firewall, profiles, rules and student question

**Original-source reference:** A:195–231.

**Instructor (A:195–204):** Ab Windows Defender Firewall check karte hain. Run dialog mein `firewall.cpl` type karne se firewall console aa sakti hai. Network settings se bhi relevant control milta hai. Firewall profiles aur enabled/disabled states ko dekhiye. Instructor green security status ki baat karte hain aur batate hain ke default mein firewall on ho sakti hai; production policy change karne se pehle zaroorat aur impact samjhein.

**Instructor (A:205–213):** 'Turn Windows Defender Firewall on or off' jaise options aate hain, lekin sirf experiment ke liye firewall disable mat karein. 'Block all incoming connections, including those in the list of allowed apps' ka option allowed exceptions ko bhi block kar sakta hai; is se connectivity toot sakti hai. Advanced firewall console mein inbound aur outbound rules ko granular tareeqe se configure kiya jata hai.

**Instructor (A:214–226):** Classroom mein policy aur organization-wide configuration par baat hoti hai. Kisi company ke server par Windows firewall off dikhne ka matlab yeh ho sakta hai ke doosra network security architecture deploy hai, lekin isey automatically safe assume nahin karna. Client-server connectivity ke liye ports, service requirements aur policy ko consider karna hota hai.

**Student / Instructor (A:227–231):** Sarfraz ji firewall aur file server connectivity par sawal karte hain. Instructor unhein yaad dilate hain ke group policy se domain machines par rules manage kiye ja sakte hain. Student kehta hai, 'Haan, mera answer clear ho gaya.' Lecture mein yeh point aata hai ke firewall enable rakh kar bhi file-sharing services ke liye required rules allow kiye ja sakte hain.


---

# Day 03 Part A — Enterprise readiness, PAM and server auditing

**Original-source reference:** A:232–273.

**Instructor (A:232–241):** Main students se poochta hoon ke pace sahi hai ya topics bohat zyada lag rahe hain. Mera goal sirf installation ka button click karwana nahin; enterprise mein server build ka real environment samjhana hai. Aap jab company join karte hain to roles, permissions, auditing, monitoring aur approvals bhi important hote hain. Kai administrators ne server install karna seekha hota hai magar production procedure se waqif nahin hote.

**Instructor (A:242–253):** Ek common galti yeh hai ke administrator seedha high-privilege account se server login kar leta hai. Organizations privileged access ko control karne ke liye PAM tool use kar sakti hain. Password kisi notebook mein ya common static credential ke taur par rakhne ke bajaye, managed vault se temporary ya rotated password diya ja sakta hai.

**Student / Instructor (A:249–257):** Student ka sawal hai: 'Agar password khud set kar sakte hain to tool generate kyun kare?' Instructor jawab dete hain ke tool ka maksad sirf password banana nahin: authorized access, rotation, time-bound use aur activity accountability hai. Student pooch sakta hai ke AD account already available hai to PAM kyun? Instructor dikhate hain ke AD identity aur privileged session authorization alag controls ho sakte hain.

**Instructor (A:258–264):** PAM ke through session start ho to company kuch systems mein screen/session recording aur detailed audit log capture karti hai. Agar kisi ne reboot kiya aur baad mein mana kar diya, authorized audit trail incident review mein help karta hai. Yahan privacy, policy aur role-based controls ka khayal rakhna lazmi hai.

**Instructor (A:265–273):** Teaching ke dauran kabhi naya idea ya issue aaye to main note bana leta hoon. Classroom mein occasional troubleshooting aa jaye to use learning opportunity samjhein. Mere liye professional learning ka matlab questions se ghabrana nahin, balki systematic exploration karna hai.


---

# Day 03 Part A — Student AI questions, Python and automation examples

**Original-source reference:** A:274–323.

**Instructor (A:274–283):** Aaj information ki availability bohat asaan ho gayi hai. Google, documentation aur AI tools se hum kisi topic ko multiple angles se samajh sakte hain. Students ko suggest karta hoon ke AI prompts ka useful istemal seekhein—lekin answer ko environment mein verify bhi karein. Main ChatGPT, Claude aur Gemini ka zikr karta hoon aur kehta hoon ke ek hi question ke answers compare kar sakte hain.

**Instructor (A:284–297):** Ek tool ne answer simple diya ho aur doosra detail de to dono ko cross-check karna learning ka hissa ban sakta hai. Group mein bhi discussions share karein, magar messages relevant aur professional rakhein. WhatsApp group ko spam aur unrelated chat se bharne ki bajaye learning notes aur genuine technical questions ke liye rakhein.

**Student (A:298–303):** Sir, maine coding question ChatGPT aur Claude dono ko diya. Mere experience mein Claude ka free version zyada useful code explain kar raha tha jabke paid ChatGPT ka jawab utna helpful nahin tha. Main Python coding ki baat kar raha tha.

**Instructor (A:303–316):** Main bhi automation par kaam karta hoon. Manual registration process mein pehle email, WhatsApp ya phone reminder bhejne padte the. Ab experiment kar raha hoon ke form submission ke baad automatically email trigger ho, messages generate hon aur Azure/Meta type integrations se workflow simplify ho. Market mein ready-made third-party solutions bhi hain, lekin kabhi direct integration bana kar learning hoti hai. AI se ek approach ke bajaye multiple options mil sakte hain.

**Instructor (A:317–323):** AI ko sirf images edit karne ya casual questions ke liye mat rakhein; system administration ki daily practice, scripting, documentation aur diagnostics mein bhi uska thoughtful use ho sakta hai. Jo bhi command AI suggest kare, usay bina samjhe production server par run na karein.


---

# Day 03 Part A — DHCP scripts, IP leases and shortcut techniques

**Original-source reference:** A:324–350.

**Instructor (A:324–333):** Agle classes mein shell/PowerShell scripts aur DHCP examples share karne ka plan hai. DHCP ka purpose network devices ko dynamically IP address assign karna hai. Lease period ke baad address pool mein release/renew ho sakta hai. Kabhi bade environment mein stale leases, bad-address entries ya pool exhaustion jaisi problems saamne aati hain. Instructor kehte hain ke is tarah ki practical problems ke liye automation scripts useful hain. Exact script ki recording yahan available nahin; is liye usay fabricated command ke taur par include nahin kiya gaya.

**Instructor (A:334–340):** Students ke saath friendly rehna aur professional boundary maintain karna dono important hain. Aaj hum VMware Tools install kar chuke hain aur server ki basic management side explore ki. Ab VM ko shutdown karne ki demonstration dekhte hain.

**Instructor (A:341–350):** VMware Tools ki wajah se graphics aur integration improve huin. Saath kuch host/guest keyboard shortcuts discuss kiye jaate hain. Instructor kehte hain ke woh jab bhi koi shortcut use karenge, class ko batayenge; chhoti shortcuts daily administration mein kaafi time bacha sakti hain.


---

# Day 03 Part A — Windows Server shutdown reason and planned downtime

**Original-source reference:** A:351–369.

**Instructor (A:351–356):** Main Windows Server ke desktop par `Alt+F4` press karke shutdown dialog kholta hoon. Ab shutdown reason ke bare mein message dikhta hai. Server ke shutdown ko ordinary laptop shutdown jaisa nahin samajhna chahiye. Server aksar business applications aur users ko services provide kar raha hota hai, is liye planned maintenance aur proper approval zaroori hai.

**Instructor (A:357–363):** Maintenance, hardware replacement, OS recovery, storage reconfiguration ya kisi approved task ke liye server shutdown karna pad sakta hai. Reason ko record karna change tracking ke kaam aata hai. Instructor Windows Server aur VMware ESXi guests ke behavior compare karte hain. VM console par shortcut ka effect desktop focus aur context ke mutabiq hota hai.

**Instructor (A:364–369):** Server accidentally shutdown bhi ho sakta hai; isi liye administrative permissions aur change procedures thoughtfully design honi chahiye. Production mein shutdown/reboot se pehle impacted services, approval, rollback, team communication aur post-change verification ko checklist ka hissa banayein.


---

# Day 03 Part A — Real incident: accidental shutdown, audit, RCA and PIP

**Original-source reference:** A:370–421.

**Instructor (A:370–379):** Ab ek real project incident share karta hoon. Night shift mein ticket assign hui, team member server par login hui. Task asal mein basic L1 nature ka tha, lekin project arrangement ke mutabiq team ko higher privilege/L3 access bhi mil sakta tha. Work complete karte waqt server galti se shut down ho gaya. Kuch minutes baad server phir start kar diya gaya; lekin woh minutes bhi customer ki nazar mein downtime thay.

**Instructor (A:380–389):** Agle din client ki email aayi. Mujhe investigate karna pada ke exactly kis waqt server off hua aur kisne kiya. Audit/session recording ke available tool se footage dekhi gayi aur event verify hua. Employee ke saath baith kar incident samjha; phir management aur customer ko explanation/RCA deni padi. Important lesson yeh hai ke 'server five minutes hi down tha' bhi production mein trivial nahin hota.

**Instructor (A:390–399):** Story yahin khatam nahin hui. Agli shift ke kisi aur user ne WhatsApp, Teams ya email communication time par nahin dekhi aur situation ko confuse kar diya. Instructor shift handover aur huddle meeting ka zikr karte hain. Huddle mein incoming/outgoing teams tasks, open incidents aur change instructions clear karti hain. Proper handover na ho to ek issue dobara repeat ya mishandle ho sakta hai.

**Instructor (A:400–415):** Management kabhi disciplinary action, removal from assignment, ya PIP (Performance Improvement Plan) ka zikr kar sakti hai. Instructor apne experience aur opinions share karte hain ke performance concerns kaise address hote hain. Isko har organization ki universal HR policy na samjhein. Lekin clear fact yeh hai ke incident, escalation aur documentation ko calmly, accurately aur professionally handle karna chahiye. Naye aur experienced dono administrators se errors ho sakti hain.

**Instructor (A:416–421):** Is liye main hamesha kehta hoon ke sirf technical commands nahin, enterprise behavior, responsibility aur communication bhi seekhein. Class ke baqi discussions mein is point par zor diya gaya.


---

# Day 03 Part A — International calling question, break and closing discussion

**Original-source reference:** A:422–453.

**Instructor / Student (A:422–438):** Class ke aakhir mein Sarfraz ji se telephone calls ka issue discuss hota hai. Instructor kehte hain ke unki taraf se call connect nahin ho rahi, jabke Sarfraz ki incoming call aa jati hai. Country code `+91` ya `0091` save karne ki baat hoti hai. Student batata hai ke mumkin hai number different format mein save hua ho. Dono practical alternative choose karte hain: Teams ya WhatsApp call kar lena, unnecessary international calling charges se bachna.

**Instructor / Students (A:439–453):** Instructor kehte hain ke ab das minute ka break lete hain; uske baad class continue hogi. Time-zone difference bhi discuss hota hai: ek location par morning hai aur doosri par evening/night. Instructor ki additional update aur students ka acknowledgement hota hai. Yeh classroom ki natural closing/break exchange hai, technical lecture ka hissa nahin, lekin sample ki tarah is conversation ko bhi omit nahin kiya gaya.
