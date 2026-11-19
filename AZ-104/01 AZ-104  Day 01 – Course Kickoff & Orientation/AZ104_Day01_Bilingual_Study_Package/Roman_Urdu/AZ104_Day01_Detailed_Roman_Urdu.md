# AZ-104 — Day 01 | Detailed Roman Urdu Class Notes

> **Source:** asli `AZ-104-day-01.txt` lecture. Yeh **detail ke saath topic-wise Roman Urdu rendition** hai, har jumlay ki literal translation nahin. Original transcript ZIP mein bilkul unchanged hai. Automatic transcription mein speaker identification clear nahin, is liye invented names assign nahin kiye gaye.

## 1. Class ka aghaz aur participants ka introduction

Instructor ne class shuru karte hue har student se kaha ke apna introduction dein aur batayein ke cloud computing ka course kyun join kiya. Ek participant ne bataya ke unka background non-IT hai, woh Linux seekh rahe hain, RHCSA exam pass kiya hai aur ab IT mein job ke liye cloud skills develop karna chahte hain. Instructor ne location aur pehle profession ke bare mein bhi poocha. Doosre participant ne oil and gas se IT, Linux/Unix, DevOps, SRE, observability aur banking environment tak apne safar ka zikr kiya.

Yahan class ka important point tha: **students ka experience alag alag hota hai; fundamentals se start karna zaroori hai.**

Instructor ne apna slogan **“Learn, Earn, and Grow”** share kiya. Unhon ne Windows Server, Exchange, VMware, Azure, corporate training, data-center architecture aur solution design mein apne experience ka zikr kiya. AS Network Zone aur System SLA Technologies ka bhi introduction diya. Yeh instructor ke apne bayan hain, independently verified details nahin.

## 2. AZ-104 ka purpose aur certification roadmap

Instructor ke mutabiq training ka maqsad sirf Azure portal par clicks seekhna nahin hai. Aapko **infrastructure administrator aur data-center architect** jaisi soch develop karni hai.

Unhon ne **AZ-900** ko fundamentals, **AZ-104** ko Azure administration, aur **AZ-305** ko architecture-related aglay step ke taur par discuss kiya. Transcript mein ek jagah “AZ-400” bhi aata hai, lekin session ka overall context AZ-104 hai. Class schedule ko unhon ne shorter daily sessions ke saath taqreeban six-week course ke taur par samjhaya.

### Course ke central areas

- **Identity and governance:** users, access, cloud policies aur organizational requirements.
- **Storage:** storage ki types aur management.
- **Compute:** Windows/Linux virtual machines aur workloads.
- **Networking:** IP addresses, subnetting, CIDR, VLSM, VNet, routing, switching aur firewalls.
- **Monitoring:** CPU, memory, storage usage, health, resources aur billing.

Instructor ne **Azure Virtual Desktop (AVD)** ka introductory example bhi diya. Is ka purpose users ko centrally hosted desktop environment dena hai. VMware Horizon aur VDI ko comparison ke taur par discuss kiya. Desktop support aur server administration ke tasks overlap kar sakte hain, magar dono bilkul same role nahin.

## 3. L1, L2, L3 aur architect responsibilities

Lecture mein L1 se L3/L4 tak increasing responsibility ki baat hui: basic user support, operations, advanced troubleshooting aur architecture. Yaad rakhein ke **certification aur corporate support level ki exact mapping universal nahin hoti**. Employer ke roles aur job description dekhne hote hain.

## 4. Traditional IT se virtualization aur cloud tak

Instructor ne samjhaya ke pehle organizations physical servers khareed kar data center mein install karti thin. **Traditional IT** mein hardware, cooling, power, rack, networking, security aur staff sab plan karna padta tha.

**Virtualization** mein ek physical host par multiple virtual machines chal sakti hain. Is se hardware utilization improve ho sakti hai. **Cloud computing** mein provider ki infrastructure aur services agreed billing aur responsibility model ke saath consume ki jati hain.

Instructor ne bicycle, motorcycle aur car ka example diya: jaise insan ki zarooriyat aur capability barhti hain, usi tarah IT mein platform aur kharchay badalte hain. Lekin infrastructure ki planning aur operations ki responsibility khatam nahin hoti.

## 5. Classroom role-play: customer ko 15 physical servers chahiye

Class ka sab se important real-world scenario yeh tha ke hum sab **shared data-center provider** mein kaam kar rahe hain. Sify ka naam example ke liye use hua. Customer **15 naye physical servers** install karwana chahta hai.

Students ne pehle CPU, RAM, storage, network, applications aur 24x7 support ka zikr kiya. Instructor ne samjhaya ke sirf hardware specification poochna kafi nahin. Sab se pehle customer ki **business services aur workloads** samajhne hain.

### Customer se kya poochna hai?

1. **15 servers hi kyun?** Capacity calculation hui hai ya rough estimate hai? 12, 15 ya 17 servers ki actual zaroorat ho sakti hai.
2. In par **kaun si services** chalengi — DNS, DHCP, Domain Controller, web, database, file ya print services?
3. Har service ki CPU, RAM, storage aur network requirement kya hai?
4. Future growth aur redundancy ka plan kya hai?
5. Hardware customer provide karega ya data-center provider?
6. Remote management chahiye? Physical access aur security rules kya honge?
7. Support, outage handling aur SLA agreement kya hoga?

Instructor ne professional wording par bhi zor diya: “Aap kin **services** ke liye servers chahte hain?” kehna, sirf “kaun si applications install karni hain?” se zyada business-focused sawaal ho sakta hai. Halaanke technical taur par workloads aur applications bhi bilkul valid terms hain.

## 6. Customer ki nazar se data-center checklist

### A. Location aur disaster risk

Servers **kis geographic location** par rakhe jayenge? Flood, earthquake, state-wide disruption ya travel restriction ki surat mein kya backup plan hai? Disaster recovery kis site par hogi?

### B. Cooling aur environment

Cooling, airflow, humidity aur monitoring ka arrangement kaisa hai? Agar cooling fail ho jaye to kya hoga? Instructor ne English-speaking environment ki analogy se bataya ke acha **environment** performance aur learning dono ko affect karta hai. Recording mein jo unusual temperatures discuss hue, unhein recommended operating standard na samjhein.

### C. Power redundancy

Utility feed, UPS, generator, **PDU (Power Distribution Unit)** aur dual PSU ka kya arrangement hai? Ek power source fail ho to doosra kaise kaam karega? Kya dual supplies separate feeds par hain?

### D. Rack placement

Kya **saare 15 servers ek hi rack** mein rakhenge? Agar us rack ka PDU down ho gaya to sab servers affect ho sakte hain. Different racks aur power paths mein distribution ka plan evaluate karna chahiye.

### E. Physical security

Shared facility mein customer servers ka owner ho sakta hai, lekin usay unrestricted physical access zaroori nahin milta. Instructor ne escorted visits, customer isolation, cleanliness aur shared network cables ki protection explain ki.

### F. Remote management

Kya server ko remotely access kiya ja sakta hai? Kya data center remote-hands support provide karta hai? Physical visit ke baghair approved administrators troubleshooting kar saken — yeh bhi planning ka hissa hai.

## 7. Private aur shared/public data center

**Private data center:** company apne servers aur network equipment ko apne kaam ke liye own/manage karti hai. Instructor ne System SLA aur AS Network Zone ko example ke taur par liya.

**Shared/colocation data center:** provider ki facility mein multiple customers apne servers ya rented equipment rakh sakte hain. Conditions, charges aur physical access rules provider ke contract par depend karte hain.

**Important:** Colocation aur public cloud ek cheez nahin hain. Cloud mein abstraction, self-service aur service model ki kuch additional khasusiyat hoti hain.

## 8. CAPEX aur OPEX

**CAPEX = Capital Expenditure:** infrastructure ki up-front capital investment, jaise servers aur major equipment.

**OPEX = Operating Expenditure:** recurring running expenses, jaise electricity, salaries, maintenance aur subscriptions.

Instructor ne emphasis diya ke business ko sirf server purchase ka bill nahin dekhna chahiye; location, support, security, licensing aur ongoing costs bhi plan karne hain. Ek technical clarification: baad mein purchase kiya gaya naya physical server bhi accounting ke hisaab se CAPEX ho sakta hai; har later expense OPEX nahin hota.

## 9. SLA aur P1–P5 priorities

Class ke akhir mein **SLA — Service Level Agreement** samjhaya gaya. Agar 15 mein se ek server down ho jaye, provider kitni jaldi acknowledge karega aur kitni jaldi service restore karne ka target rakhega?

Instructor ne **P1, P2, P3, P4 aur P5** priority categories discuss keen. Unhon ne samjhaya ke **P = Priority** hota hai aur urgency/business impact se determine hoti hai. Misal ke taur par 1,200 employee accounts create karne ka bulk request planning ke saath low-priority ho sakta hai, jabke production outage urgent ho sakta hai.

Lecture mein kuch **illustrative timings** aaye: P1 ticket ke liye roughly 5–10 minutes mein response, doosre priorities ke liye comparatively zyada waqt. Yeh numbers har company ka universal rule nahin hain.

- **Response SLA:** ticket receive hone ke baad acknowledgment ya initial action mein kitna waqt laga.
- **Resolution/Restoration SLA:** issue resolve karne ya service restore karne ka agreed target.

P1 ke case mein instructor ne phone call ke zariye engineer ko alert karne ka practical example diya. Sirf ticket assign kar dena hamesha sufficient communication nahin hota.

**Lecture yahan incomplete end hota hai:** Original transcript P1 resolution-time discussion ke darmiyan ruk jata hai. Uske baad ki koi baat assume nahin ki gayi.

## 10. Lecture se important learning points

- Certification ke saath **business requirements** samajhna bhi seekhein.
- Customer aur provider dono ki nazar se questions karne ki practice karein.
- 15-server requirement ko validate karein; seedha hardware order na karein.
- Cooling, power, rack, disaster aur access controls ko architecture ka hissa samjhein.
- CAPEX/OPEX aur **response vs resolution SLA** mein clear difference rakhein.
- Technical interview mein practical examples ko structured jawab mein badlein.

> Additional labs, interview questions aur verified corrections alag files mein hain. Woh instructor ke original alfaaz nahin hain.
