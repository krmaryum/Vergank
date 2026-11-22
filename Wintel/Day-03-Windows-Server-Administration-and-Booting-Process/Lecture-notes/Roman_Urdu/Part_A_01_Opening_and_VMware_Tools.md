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
