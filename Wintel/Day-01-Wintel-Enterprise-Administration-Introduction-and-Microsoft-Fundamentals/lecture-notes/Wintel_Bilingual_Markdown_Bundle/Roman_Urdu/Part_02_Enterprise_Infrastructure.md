# Wintel Training Class — Roman Urdu Translation
## Part 02: Enterprise Roles, Server Builds, aur Company ka Practical Scenario

**Source:** `Wintel_English_Translation_Part_02.md` aur asal `wintel.txt`, taqreeban lines 132–253.

**Note:** Yeh mukammal Part 2 ka tafseeli Roman Urdu tarjuma hai, summary nahin. Asal class ka order, participants ki guftagu, examples aur technical terms barqarar hain. Kuch source speaker labels ghalat ya mixed ho sakte hain; unhein source ke qareeb rakha gaya hai.

## 1. Identity and Access Management: Enterprise ki Misaal

**Speaker 1 (Instructor):** Hamare paas mukhtalif qisam ki services hoti hain. Misaal ke taur par company ke andar humein **Identity and Access Management** ki zaroorat hoti hai. Main yeh term is liye use kar raha hoon ke jab hum aage chal kar in concepts ko cloud computing ke saath connect karenge to aapko cheezen zyada achhi tarah samajh aayengi. Humein **User Management** bhi karni hoti hai.

Aaiye tasawwur karte hain ke hum sab ek organization mein administrators hain aur alag alag teams mein kaam karte hain. **Nadeem storage** handle karte hain, **Khalid virtualization** dekhte hain, aur **Sarfraz physical servers**, jaise HP aur Dell servers, manage karte hain. Jab bhi humein koi naya physical server chahiye hoga, hum Sarfraz se contact karenge. **Anil operating systems** ke responsible honge, jaise Windows Server aur Linux.

Aaj ki discussion ko general rakhte hain taa-ke basic concepts clear ho jaayein. Aap maan lein ke main **Data Center Architect** hoon aur main aap sab se kaam coordinate karwaunga. Nadeem storage team mein honge. Khalid virtualization handle karenge, chahe Hyper-V ho ya VMware. Sarfraz physical hardware dekhenge aur Anil server operating systems ka kaam dekhenge.

Ab yeh bhi sochiye ke aap mein se har shakhs apni team ka architect hai. Aapke neeche do log ho sakte hain, paanch ho sakte hain, ya pandrah bhi ho sakte hain. Jaise jaise project bara hota jayega, team bhi expand ho sakti hai. Aur jab project ka kaam poora hota jayega to team ki size kam bhi ki ja sakti hai.

## 2. Labs ke Liye Ek Example Company Banana

**Speaker 1:** Maan lein ke hum ek nayi company setup kar rahe hain. Main misaal ke liye apni company use karunga. Is poore course mein hum **same company aur same domain naming** use karenge taa-ke hamare saare labs ek consistent scenario ka hissa banein.

Maan lein maine ek startup banaya hai jiska naam **System SLA Technologies Private Limited** hai. Yeh IT ki company hai jo **Technical Support Services** provide karti hai. Hum is company ki website par kaam kar rahe hain taa-ke woh zyada professional nazar aaye. Company ka main kaam IT support dena hai.

Ab is startup ne administrators hire kar liye hain. Agla kaam yeh hai ke humein company ke liye **Data Center implement** karna hai. Mujhe umeed hai aap sab jaante honge ke Data Center kya hota hai. Anil, kya aapne kabhi Data Center physically visit kiya hai?

**Speaker 3 (Anil):** Nahin sir, main poori tarah remote kaam karta hoon. Lekin mujhe maloom hai ke Data Center woh jagah hoti hai jahan servers rakhe jaate hain aur applications host ki jaati hain.

**Speaker 1:** Theek hai. Sarfraz?

**Speaker 3 (source ke label ke mutabiq):** Sir, main apni company ka Data Center khud manage kar raha hoon.

**Speaker 1:** Perfect. Main aap logon ke saath Data Centers ki kuch clips aur videos bhi share karunga taa-ke aap dekh sakein ke infrastructure asal mein kaisa hota hai. Kuch cheezen sirf sunne se nahin, balke apni aankhon se dekhne ke baad zyada clearly samajh aati hain.

## 3. Physical Servers Ko Dekhna Kyun Zaroori Hai?

**Speaker 1:** Maine 2006 mein Windows Server ki training li thi, aur us waqt hum **Windows Server 2003** use karte thay. Is naye course mein hum **Windows Server 2022 aur Windows Server 2025** dono use karenge, yani ek mixed environment mein training hogi. Aage main bataunga ke humne yeh dono versions kyun choose kiye hain.

Jab maine pehli dafa Windows Server seekha to mujhe samajh aa gaya tha ke **Active Directory, DNS, dial-up, VPN, IAS, FTP aur router** kya hote hain. Maine networking ki training bhi li thi, jisme CCNA shamil tha. Lekin us waqt bhi mujhe yeh nahin pata tha ke production environment mein ek asli physical server dekhne mein kaisa hota hai.

Maine qareeban 2007 mein interviews dena shuru kiye. Windows Server, Exchange Server aur networking ki kai mahine training ke baad main jobs dhoondh raha tha. Kaafi arse tak maine physical server ko directly handle nahin kiya tha. Qareeban 2009 mein maine pehli dafa Google Images par physical servers ki tasveeren dekheen.

Aaj bhi aapko aise IT professionals mil sakte hain jo 18, 24 ya 25 saal se industry mein kaam kar rahe hon, magar unhein physical server dekhne ka mauqa kabhi na mila ho. Yeh mumkin hai kyunke unka saara kaam remote hota hai. Iska matlab yeh nahin ke unka kaam galat hai; bas unko physical hardware ke saath kaam karne ka mauqa nahin mila.

AS Network Zone mein hamare paas kuch physical servers hain. Aapko in par labs karne ka mauqa milega. Hum physical server hardware ke saath kaam karne ke liye zaroori concepts bhi padhenge.

Interview mein ek common sawal pehle bhi poochha jata tha aur ab bhi poochha jata hai: **"Kya aapne kabhi naya server configure ya build kiya hai?"** Kuch experienced candidates iska jawab haan mein de sakte hain. Lekin bohat se log jo remote preconfigured servers par kaam karte hain, unhein aisa hands-on experience nahin milta.

**Speaker 2:** Ji sir, yeh sawal interviews mein aata hai. Aap sahi keh rahe hain, mujhe lagbhag har interview mein yeh question sunne ko milta hai.

**Speaker 1:** Mujhe nahin maloom ke Nadeem aur Khalid ne physical servers par kitna kaam kiya hai. Remote system par login kar ke kaam karna alag baat hai. Lekin tasawwur karein ke aapke saamne company ka ek **brand-new physical server** aa gaya. Ab aapko uska complete build karna hai aur requirement ke mutabiq **Windows, Linux ya ESXi** install karna hai. Interviewer aapse poochh sakta hai ke poora **Server Build Process** kya hai.

## 4. Instructor ka Career aur Server Build Experience

**Speaker 1:** Maine 2007 se 2016 ke darmiyan HCL mein kai baar interviews diye. 2016 mein mera selection ho gaya, lekin us waqt maine HCL join nahin kiya; uske bajaye IBM join kiya. Phir 2019 mein dobara HCL ka interview diya aur is baar join kar liya. Main 2025 tak HCL mein kaam karta raha. Iske baad 2025–2026 mein Times Group ke saath associated raha. October ke aakhir mein maine wahan ki job chhor di aur ab poori tarah System SLA ke saath kaam kar raha hoon.

System SLA meri private company hai. Iske through main projects leta hoon aur un par kaam karta hoon. Mujhe khud projects par practical kaam karne mein maza aata hai. Saath hi meri company se mujhe employment ke muqable mein zyada earning hoti hai. Training dena mera passion hai, is liye main teaching continue rakhta hoon.

Interview mein ab bhi ek bohat important sawal poochha jata hai: **"Aap server kaise build karte hain?"** Jab main beginner tha to main samajhta tha ke server build karna matlab **CD ya DVD lagana, Windows Server install karna, aur required server role configure kar dena**. 2006–2007 ke zamane mein laptops itne aam ya asani se available nahin thay, is liye main desktop aur installation media ka sochta tha.

Aaj bhi kuch training courses sirf Operating System ki installation sikha kar usko server training kehte hain. Lekin asal baat yeh hai ke **production server build karna sirf Operating System install karne ka naam nahin hai.**

## 5. Complete Production Server Build Mein Kya Kya Hota Hai?

**Speaker 1:** Shuru mein mujhe lagta tha ke Windows Server install karne mein aadha ghanta lagega, phir server ready ho jayega. Lekin jab main companies mein kaam karne laga to maloom hua ke ek naya server build karne ka **SLA aath ghante** ka bhi ho sakta hai. SLA ka matlab **Service Level Agreement** hai.

Anil, kya aapne kabhi naya server build kiya hai, ya remote par kisi aur ko naya server build karte hue dekha hai?

**Speaker 3 (Anil):** Nahin sir. Hamare systems pehle se configured hote hain. Hum bas login karte hain aur apna kaam shuru kar dete hain. Mujhe server build karne ka hands-on mauqa nahin mila.

**Speaker 1:** Yeh bohat common problem hai. Interview mein humse bohat saare sawal kiye jaate hain, lekin jab hum kisi organization mein join karte hain to infrastructure pehle se configured milta hai. Humein har baar yeh dekhne ka mauqa nahin milta ke woh infrastructure start se kaise deploy hua tha.

Ek complete server build mein aam taur par yeh kaam shamil ho sakte hain:

1. **Remote Management Configuration:** Physical server ke remote management interface, jaise **iLO**, ko configure karna.
2. **RAID Configuration:** Server ki disks ke liye RAID storage setup karna.
3. **Firmware Updates:** Server ke hardware firmware ko update karna.
4. **Operating System Installation:** Requirement ke mutabiq Windows Server, Linux ya doosra OS install karna.
5. **Monitoring Agents:** Monitoring ke agents install karna taa-ke server ki health aur performance check ki ja sake.
6. **Security Patching:** Security patches aur Operating System updates install karna.
7. **Domain Join:** Zaroorat ke mutabiq server ko company ke domain mein join karna.
8. **Roles, Features aur Permissions:** Required server roles, features aur access permissions configure karna.
9. **Network Team Coordination:** Network team ke saath mil kar IP address aur doosri network settings assign karna.
10. **Security Team Coordination:** Antivirus aur doosre security controls ke liye security team ke saath kaam karna.

Is process mein multiple teams participate kar sakti hain. Isi liye server build ka agreed SLA sirf OS installation ke waqt se kahin zyada ho sakta hai.

## 6. Server Build ke SLA Mein Extra Buffer Time Kyun Hota Hai?

**Speaker 1:** Ab maan lein ek server build ka kaam subah **11:30 baje** shuru hona hai aur shaam **6:30 ya 7 baje** tak deliver karna hai. Is darmiyan aapke paas doosre tasks aa sakte hain. Calls, meetings, breaks, lunch, ya shift handover ki responsibilities bhi ho sakti hain. Agar aapko lagta hai ke aap task complete nahin kar payenge to aapko kisi doosre team member ko handover kar dena chahiye taa-ke SLA breach na ho.

Agar main lagataar ek hi server build par kaam karoon to mumkin hai ke **chaar ya paanch ghante** mein complete kar doon. Lekin companies kabhi kabhi **aath ghante** ka SLA rakhti hain taa-ke delays ko handle karne ke liye buffer available ho.

Physical servers ko reboot hone mein aam desktop ya laptop ke muqable mein zyada waqt lag sakta hai. Patches install karne ke baad restart mein **10, 15 ya 20 minutes** bhi lag sakte hain. Isi waqt koi meeting, call ya doosra task bhi aa sakta hai. Isi liye kaam ko plan karna aur buffer time rakhna zaroori hai.

Course aage barhne ke saath main aapko bataunga ke companies mein yeh kaam **systematic aur professional tareeqe** se kaise kiye jaate hain.

Mere beginner hone ke zamane mein interview ka ek aur sawal mujhe confuse karta tha: **"Kya aapne tools par kaam kiya hai?"** Us waqt mujhe samajh nahin aata tha ke interviewer kis tarah ke tools ki baat kar raha hai. Tajurbe ke saath insaan sawal ko samajhne aur solution dene mein behtar ho jata hai. Behtar yeh hai ke pehle saamne wale ki poori problem dhyan se sunein aur uske baad jawab ya solution dein, bajaye iske ke foran beech mein bol dein.

## 7. Dobara Company ke Practical Scenario par Aate Hain

**Speaker 1:** Ab hum wapas apne startup aur un mukhtalif teams ki misaal par aate hain jo humne banayi theen.

Hello Gautam. Maaf kijiye, humne pehle aapko welcome nahin kiya. Shayad aap thora late join hue. Abhi humne apna course shuru hi kiya hai aur discussion kar rahe hain ke companies mein infrastructure kaise deploy hota hai aur teams kaise kaam karti hain.

**Speaker 2 (Gautam, source label):** Hello sir. Ji sir, theek hai.

**Speaker 1:** Ab maan lein hamari company apna naya business setup kar rahi hai. Company apne employees ke liye bhi kuch infrastructure deploy karegi.

**Identity and Access Management** ke liye hum **Active Directory Domain Services (AD DS)** padhenge. Domain ke andar names resolve karne ke liye **DNS** chahiye hoga. Computers ko IP address settings provide karne ke liye **DHCP** ki bhi zaroorat hogi.

Agar hum company ki website ya doosri applications publish karte hain to **Web Services** chahiye hongi. Agar secure access required ho to hum public service ko plain **HTTP** par nahin chalana chahenge; hum **HTTPS** use karenge. Iske liye certificates chahiye hote hain. Hum **Certificate Authority (CA)** server aur certificates issue karne ke process ko bhi samjhenge.

Yeh un servers ki misaalein hain jo **System SLA Technologies** apne employees aur internal operations ke liye deploy kar sakti hai. Iske baad hum discuss karenge ke company customers ko technology services provide kar ke revenue ya earning kaise karti hai.

---

**Part 02 khatam.** Original transcript ka agla hissa IT services ki selling, IT resources, Project Management, IBM ke hypothetical bank project aur Data Center planning se related hai.

**Editorial note:** Yeh instructor ki class ka Roman Urdu tarjuma hai, independent technical fact-check nahin.
