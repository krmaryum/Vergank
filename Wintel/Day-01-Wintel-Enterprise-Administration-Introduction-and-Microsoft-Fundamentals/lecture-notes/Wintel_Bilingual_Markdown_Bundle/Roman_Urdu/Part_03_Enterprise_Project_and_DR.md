# Wintel Training Class — Roman Urdu Translation
## Part 3: Enterprise Project Planning, Data Centers, Hardware Support aur Disaster Recovery

**Original transcript:** `wintel.txt`, lines **254–496**.  
**Tarjume ka tareeqa:** Class ki detailed discussion, instructor ke examples, students ke sawalat, numbers aur sequence ko preserve kiya gaya hai. Sirf short summary nahin banayi gayi. Jahan transcription mein speaker ya koi lafz unclear hai, wahan meaning ko ehtiyat se likha gaya hai.

---

### 1. IT Support Company Paisa Kaise Kamati Hai?

**Instructor (Speaker 1):** Ab tak hum baat kar rahe thay ke company apne employees ko infrastructure kaise provide karti hai. Lekin ab sawal yeh hai ke company revenue kaise earn karegi? Humne kaha ke System SLA Technologies ek IT technical support company hai. To yeh company paisa kaise kamayegi? Kisi ko idea hai?

**Participant (Speaker 2):** Sir, hum apni services publish karenge. Logon ko batayenge ke hum yeh service provide karte hain, woh service provide karte hain, aur customers ko apni offerings ke bare mein inform karenge.

**Instructor:** Bilkul correct. Hum apni website par services publish kar sakte hain. Misaal ke taur par kisi ne naya startup shuru kiya hai. Hum usay keh sakte hain, “Aap ko website chahiye to hum bana kar denge.” Agar storage chahiye, hum storage provide karenge. Servers ki requirement hai to servers denge. Networking infrastructure ki zaroorat hai to woh bhi provide karenge.

Ho sakta hai kisi company ko technical support team chahiye, lekin us ke paas apni team hire karne aur maintain karne ke liye budget, resources ya authorization na ho. Hamare paas pehle se technical team maujood hai. Hum apne employees ke zariye us company ko support provide kar sakte hain.

Aap ne dekha hoga ke kuch log kehte hain, “Main IBM mein kaam karta hoon lekin meri primary company koi aur hai.” Ya koi kehta hai, “Mujhe salary HCL deta hai lekin main HCL ki taraf se IBM ke project par support de raha hoon.” IT industry mein is tarah ke third-party arrangements bohat common hain.

### 2. IT Project Mein Resource Ka Matlab

**Instructor:** Ek important term yaad rakhiye: **resource**. Project ke andar bohat si cheezon ko resource kaha jata hai. Company ke employees ko bhi project planning ki language mein resources kaha jata hai.

Misaal ke taur par Nadeem storage team ka resource hai, Khalid virtualization team ka resource hai, Sarfraz physical server infrastructure ka resource hai, aur Anil Windows/Linux operating-system team ka resource hai.

Yahan resource se murad koi aisi cheez ya shakhs hai jis se project ka kaam complete karne ya service deliver karne mein madad li jati hai. Is lecture mein hum yeh term bar bar use karenge.

Aaj hum jaan boojh kar Windows Server ke core technical topics mein nahin ja rahe. Pehle basic fundamentals samajhna hain: real companies kis tarah projects leti hain, teams banati hain aur infrastructure implement karti hain.

### 3. Marketing Team, Project Lana aur Certifications

**Instructor:** System SLA Technologies apni website, Facebook/Meta, Google aur doosre platforms par advertisement kar sakti hai. Is ke ilawa marketing team hire kar sakti hai jo doosri companies ke paas jaye, services explain kare aur business ya projects lekar aaye.

Marketing team mein MBA-qualified log ho sakte hain. Kuch log BTech ya MTech background se bhi aa sakte hain aur un ke paas additional certifications hoti hain. Is class mein **PMP**, **ITIL** aur **PRINCE2** ka zikr hua. Transcript mein “AZIL” jaisa ek lafz bhi aata hai, lekin recording se us ka exact naam clear nahin.

Instructor ke explanation ke mutabiq PRINCE2 ko structured project approach aur clients ke saath project work se relate kiya gaya. PMP project management se related certification hai: jab project mil jaye to us ko plan aur manage kaise karna hai? ITIL ke hawale se baat hui ke client ko services aur project work mein transparency milni chahiye.

In frameworks ko course mein aage detail se discuss kiya jayega. Abhi fundamental baat yeh hai ke IT company ko business lana hota hai, resources arrange karne hote hain aur customer ko promised service deliver karni hoti hai.

### 4. IBM Se Banking Project Milne Ki Example

**Instructor:** Ab assume karein ke hamari marketing team ka ek member project lekar aaya. Example ke liye yeh project IBM ki taraf se hai aur kisi bank se related hai. Samajhne ki asani ke liye is ko “IBM bank project” keh dete hain.

Marketing colleague kehta hai, “Vargank, hamare paas ek naya project aaya hai. Is bank ke liye infrastructure set up karna hai.”

IT industry mein projects US, UK ya doosre mulkon ke clients ke liye bhi hote hain. Domestic projects bhi milte hain, lekin aksar hamari support team kisi doosri geographical location par maujood infrastructure ko manage karti hai. Instructor ne bataya ke unhon ne Tech Mahindra mein Delhi Police ke domestic project par bhi kaam kiya tha; recording mein us ka date range clear nahin hai.

Misaal ke taur par aap Delhi mein rehte hain lekin Bengaluru ka project support kar rahe hain. Bengaluru ki team Chennai ka infrastructure dekh rahi hai, ya Chennai se Pune ka project manage ho raha hai. Data center kisi ek location mein hota hai, lekin us ka customer koi teesri company ho sakti hai.

Ab hamari example mein US ke ek bank ke liye **data center implement** karna hai.

### 5. Sirf Ek Windows Server Tak Soch Limited Na Rakhein

**Instructor:** Jab aap Active Directory, DNS, DHCP ya koi aur server role manage karte hain, to sirf us ek server ko apni poori duniya na samjhein. Sawal poochhein ke yeh server physically kahan host ho raha hai. Jawab hai: data center ke andar.

Ek engineer ko surrounding environment ka bhi idea hona chahiye. Mujhe nahin pata ke is waqt aap ki companies mein managers ne aap ko kitni responsibilities aur access di hui hain. Lekin meri suggestion hai ke doosri teams ke saath coordination karein, un ke kaam ko samjhein aur maximum cheezein explore karein.

Jab aap physical infrastructure, virtualization, storage, networking aur doosri supporting technologies samjhenge, tab apne server ka role bhi behtar samajh aayega. Real server-build process ki planning isi level se start hoti hai, sirf Windows installation screen se nahin.

**Instructor:** Gautam, main aap se sawal karna bhool gaya: kya aap ne kabhi naya server build kiya hai? Aap hain? Theek hai, koi masla nahin. Aage chalte hain.

### 6. Customer Ki Requirement: 1,500 Servers

**Instructor:** IBM hamari team se kehta hai: “Vargank, hamein approximately **1,500 servers** build karne hain.” Kitne servers?

**Participant:** Fifteen hundred.

**Instructor:** Ji haan, 1,500. Jab main IT mein fresher tha to mere zehan mein bhi sawal aata tha: kya companies mein itne zyada servers hote hain? Itne servers ki zaroorat kyun hoti hai? Agar aap bhi soch rahe hain to aage is par baat karenge. Windows Server ke bohat se roles hain, lekin sirf roles ki list dekh kar samajh nahin aata ke company ko hundreds ya thousands of servers kyun chahiye.

Ab thori dair ke liye apni current designation bhool jaiye. Apne aap ko **data center architect** samjhiye. IBM ne 1,500 servers ki requirement di hai. Aap IBM se agla sawal kya poochhenge?

**Instructor:** Pehle Sarfraz se poochta hoon, kyun ke woh apna data center handle karte hain.

### 7. Data Center Architect Ko Kaun Se Sawal Poochne Chahiye?

**Participant:** Sir, agar hum bilkul scratch se start kar rahe hain, to main bohat se sawalat poochunga. Kaun se network devices chahiye? Hardware ki requirements kya hain? Data center ka purpose kya hai? Disaster recovery banana hai, availability zone banana hai ya kuch aur?

Agar 1,500 servers ka requirement hai, ho sakta hai sirf 100 physical servers hon aur baqi virtual. Mujhe dekhna hoga ke kaun sa hardware purchase karna hai, processors mein kitne CPU cores honge, kitni RAM hogi aur doosri specifications kya hongi. Ek sawal ka jawab milta jayega to us ke mutabiq naye sawalat paida honge.

**Instructor:** Correct, correct. Yeh bohat achhe points hain. Lekin filhal hum networking ke detailed area mein nahin ja rahe. Hamara course server technology par hai, is liye abhi physical server aur OS-level server par focus rakhenge. Doosri technologies ka awareness zaroor hona chahiye.

### 8. Physical, Virtual aur Cloud Servers Ki Distribution

**Instructor:** Zaroori nahin ke saare 1,500 servers physical machines hon. Kuch physical servers honge, kuch virtual machines hongi, aur kuch cloud environment mein deploy honge.

Sarfraz ne around 100 physical servers suggest kiye. Ab example ko thora expand kar lete hain:

| Deployment category | Example quantity | Kahan run honge |
|---|---:|---|
| Physical servers | 200 | Physical data center mein |
| Virtual servers / VMs | 800 | On-premises physical infrastructure par |
| Cloud servers | 500 | Cloud environment mein |
| **Total** | **1,500** | Hybrid infrastructure |

Yeh lecture ko samjhane ke liye **example numbers** hain; actual production design ke liye CPU, RAM, storage aur capacity planning alag se karni hogi.

**Instructor:** Nadeem, aaj pehle cloud class mein aap ne bhi yahi kaha tha ke kuch systems physical data center mein rakh sakte hain aur kuch cloud par. Isi ko hum yahan explain kar rahe hain.

**Participant:** Achha, achha. Wonderful.

**Instructor:** Teaching ke liye pehle physical infrastructure samajh rahe hain, phir virtualization aur phir cloud. Is tarah step by step understanding build hogi.

### 9. Data Center Ki Location Decide Karna

**Instructor:** IBM ne server count bata diya, lekin abhi location decide nahin hui. Network vendor bhi finalize nahin hua. Aage ja kar Cisco, Juniper, Aruba, Arista ya koi doosra vendor choose ho sakta hai, lekin is waqt hum server-side planning par focus kar rahe hain.

Ab IBM se poochna hoga: “Aap ka data center kahan hoga? Kya aap ki apni location pehle se available hai jahan hum servers install karein?”

Agar IBM kahe ke hamare paas facility available hai, bohat achhi baat hai. Agar kahe ke nahin, aap hamein suitable jagah suggest karein, to ab hamein data center ki location search aur evaluate karni hogi.

Hamare example mein 200 physical servers par 800 virtual servers host honge. Yani approximately 1,000 systems ka relation on-premises data center se hai. Baqi 500 cloud par deploy honge. Is liye location ka faisla bohat important hai.

**Instructor:** Dekhiye, shuru humne simple server build se kiya tha aur ab data center location planning tak aa gaye hain.

**Participant:** Yes, yes.

### 10. Public Data Centers aur Colocation Ka Concept

**Instructor:** Duniya mein public ya third-party data centers bhi available hain, jahan doosri companies apna infrastructure host karwati hain. Agar aap Noida mein data centers search karein to NTT, Sify, Nextra, CtrlS aur doosre service providers mil sakte hain. Instructor ne Yotta ka bhi example diya.

Maan lijiye hamein 200 physical servers lagane hain jin par 800 virtual machines chalengi. Hum kisi data center provider se dedicated **racks** rent kar sakte hain. Agreement ke mutabiq woh hamein rack space, power, connectivity aur physical installation services provide kar sakta hai.

Rack ek physical cabinet hoti hai jahan servers aur related equipment install hote hain. Provider hamein racks allocate karega aur un mein hamare physical servers install ho sakte hain. Agar agreement ho to provider hamari taraf se physical installation bhi kar sakta hai.

Zaroori nahin ke project milte hi hum apni data-center building khud banayein. System SLA, IBM se project le kar facility aur physical operations ka kuch kaam data center specialist ko outsource kar sakti hai. Contract sign karne se pehle cost, services, performance aur responsibilities check karna zaroori hoga.

### 11. Third-Party Data Center Ko Evaluate Karna

**Instructor:** Maan lijiye hum Nextra ko choose karte hain. Aisa nahin ho sakta ke paisay de dein aur samjhein sab theek ho jayega. Hamein check karna hai ke provider hamare 200 servers ke liye proper facilities aur support de sakta hai ya nahin.

Agar 20 servers down ho jayein? Agar 50 down ho jayein? Agar poore 200 servers stop ho jayein? Client hamari company se service expect karega. Is liye data center provider ki capacity aur responsibilities ko samajhna bohat important hai.

Evaluation ke dauran authorized team members facility ka visit kar sakte hain, setup inspect kar sakte hain aur dekh sakte hain ke hamara equipment kahan install hoga. Contract mein provider ki responsibility clear honi chahiye.

Location client ki requirement ke mutabiq bhi hoti hai. Ho sakta hai hamari company Delhi mein ho, lekin IBM kahe ke data center **Los Angeles, California** mein lagana hai. Zaroori nahin ke company aur us ka data center ek hi mulk mein hon.

**Instructor:** Bataiye, kya Los Angeles mein aisa project arrange karna possible hai?

### 12. Participant Ka Real Remote Data Center Example

**Participant (Speaker 2):** Ji haan, possible hai. Mere paas ek location par rack hai jise transcript mein Ottawa kaha gaya hai. Wahan **16 physical servers** installed hain aur un par around **48 virtual machines** chal rahi hain. Hamari company ne wahan ek local consultant hire kiya hua hai.

Agar koi hardware issue aa jaye ya physical restart karwana ho to main consultant se contact karta hoon. Woh facility ki local team se coordination karta hai. Us consultant ne physically location inspect ki, setup aur contact persons document kiye, phir report submit ki. Hamne us service ke liye payment ki.

**Instructor:** Correct. Bilkul isi tarah Los Angeles mein bhi kaam arrange ho sakta hai. Wahan public data center dhoond kar rack aur services ke charges pay kar sakte hain. Zaroori nahin ke hamari poori team har waqt physically wahan present ho.

### 13. Agar Client Ke Apne Premises Par Data Center Banana Ho

**Instructor:** Ab maan lijiye IBM chahta hai ke us ke khud ke on-premises facility mein servers install hon. Is case mein approach different hogi.

Pehla kaam HR team ko dena hoga ke Los Angeles mein local **Wintel aur data center engineers** hire kare. Shuru mein System SLA chaar, paanch ya chhe engineers arrange kar sakti hai.

Sirf ek engineer kyun nahin? Kyun ke **24×7** support ek banda provide nahin kar sakta. Agar teen shifts hon, tab bhi teen log hamesha sufficient nahin hote, kyun ke leave aur absence hoti hai. Instructor ne har shift mein do team members ki availability ki baat ki aur example ke taur par around five/six engineers discuss kiye. Actual staffing coverage requirement par depend karegi.

India se ek ya do team members initial visit ke liye Los Angeles ja sakte hain. Wahan un ki meeting local hire ki gayi team ke saath hogi. Aap ne suna hoga ke kuch log project ki wajah se doosre mulk travel karte hain. Yeh us ki ek practical reason ho sakti hai.

Deployment ke dauran team site inspect karti hai, infrastructure set up karti hai aur confirm karti hai ke systems smoothly run kar rahe hain.

### 14. Contract Hiring aur Go-Live Ke Baad Team Size

**Instructor:** Kabhi doosre mulkon mein contract basis par engineers hire karte hain. Different locations ki staffing cost different hoti hai. Example ke taur par India mein kisi engineer ki annual cost seven lakh rupees ho sakti hai, jab ke abroad kisi project staffing arrangement ki cost thirty ya forty lakh rupees ya us se zyada ho sakti hai. Yeh instructor ke illustrative figures hain.

Jab project implementation complete ho jaye aur systems stable ho jayein, to operational requirement ke mutabiq contract staff ki tadaad kam bhi ki ja sakti hai. Initial project team ki jagah do, teen ya chand engineers daily support manage kar sakte hain.

Agar third-party public data center use ho raha hai aur provider on-site support khud deta hai, to ho sakta hai hamein apne local employees hire karne ki zaroorat hi na pade. Sab kuch contract ki details par depend karta hai.

### 15. New Hardware, Vendor Support aur Server Refresh

**Instructor:** Assume karein ke hamare 200 physical servers is project ke liye bilkul naye purchase kiye gaye hain. Hum enterprise production ke liye market se random purane servers nahin utha kar laga rahe.

Jab naye servers purchase karte hain, to aam tor par hardware **support agreement** bhi lete hain. Instructor ki example mein support period **five years** hai. Agar five years ke baad bhi hardware use karna ho, to one ya two years ki support extension ka option dekha ja sakta hai.

Bohat si companies physical servers ko around five ya six years baad replace karne ka plan banati hain. Kuch servers seven years tak chal sakte hain. Eight ya nine years ka use bhi kabhi ho sakta hai, lekin instructor ke mutabiq is scenario mein yeh uncommon hai. Kabhi client downtime approve nahin karta, is liye purana hardware aur zyada arsa use hota rehta hai.

Jab hardware obsolete declare ho jaye to company usay retire ya sell karke naye servers purchase karti hai. Is process ko physical server refresh ya replacement cycle keh sakte hain.

**Instructor:** Dekhiye, humne infrastructure planning par itni detail se baat kar li hai, lekin abhi tak Windows Server OS install bhi nahin kiya. Kyun? Kyun ke server build sirf OS installation ka naam nahin hai.

**Participants:** Yes, sir.

### 16. Student Ka Sawal: Public Data Center Ke Andar Ja Sakte Hain?

**Participant:** Sir, ek sawal hai. Sorry, mera gala thora kharab hai. Aap ne kaha ke agar public data center mein kisi company ke private servers rakhe hon, to company ke apne logon ko andar jane ki permission shayad na mile. Lekin kabhi representative visit kar sakta hai. To exactly access kab allowed hota hai? Mujhe is mein confusion hai.

**Instructor:** Direct physical visits aksar restricted hoti hain. Maine class mein is ko *rare token* kaha. Yani specific authorization aur valid reason ki zaroorat hoti hai. Sirf is wajah se ke servers hamare hain, har employee ko facility mein jab chahe enter karne ka right nahin mil jata.

Ek hypothetical example lete hain. Anil System SLA ka employee hai. Maan lijiye woh do ya teen saal se kaam kar raha hai aur do saal se increment nahin mila. Woh data center mein jata hai aur apna server check karte waqt galti se kisi doosri company ki cable hila deta hai, koi device band ho jata hai, ya jaan boojh kar aisa kar deta hai. Main Anil par ilzam nahin laga raha; sirf risk samjha raha hoon.

Ab nuksan ka zimmedar kaun hoga? Anil? System SLA? Ya data center provider? Yeh sawal samjhate hain ke physical access controlled kyun hota hai.

**Participant:** Ji, samajh gaya. Yeh bohat bada risk hai.

**Instructor:** Bilkul. Apni company ke data center mein bhi risk hota hai. Misaal ke taur par koi employee resign kar raha hai aur last working day par network switch band karke chala jaye. Maqsad kisi individual par shak karna nahin, balkeh access control, supervision aur security ki importance samajhna hai.

### 17. Student Ka Sawal: Andar Nahin Ja Sakte To Troubleshooting Kaise Hogi?

**Participant:** Yeh samajh aa gaya. Lekin agar hamara server down ho jaye, services band ho jayein, ya troubleshooting chahiye ho, aur hum data center ke andar nahin ja sakte, to us waqt kya karenge?

**Instructor:** Public data center provider ke apne engineers aur representatives facility ke andar maujood hote hain. Woh hamein technical support dete hain. Video call ya Microsoft Teams call par issue show kar sakte hain, apne laptop ki screen share kar sakte hain, aur available ho to server ke **iLO** remote management interface tak access mein madad kar sakte hain.

Agar iLO bhi respond nahin kar raha, to on-site engineer physical checking mein help karega. Yani aap apni location par baith kar bhi remote support receive kar sakte hain.

Mera yeh matlab nahin ke aap kabhi visit nahin kar sakte. Proper authorization se System SLA ka representative facility mein ja sakta hai. Lekin routine hardware issue ka matlab yeh nahin ke hamara employee foran andar chala jaye.

**Participant:** Achha, ab hundred percent clear ho gaya.

### 18. OEM Engineer, Supervised Repair aur Access Logs

**Instructor:** Maan lijiye HP ya Dell server ka network card ya network cable kharab ho gaya. Hum manufacturer ya vendor ke paas support case raise karenge. Phir ek **OEM engineer** data center mein aayega.

Data center provider ka ek representative OEM engineer ke saath jayega. Woh observe karega ke engineer sahi server par kaam kar raha hai aur facility ke rules follow ho rahe hain. Kaam complete hone par dono site ke process ke mutabiq bahar nikalenge.

Data center mein visit ki **log entry** bhi hoti hai. Is tarah accountability maintain hoti hai. Isi liye hardware purchase karte waqt vendor support lena important hota hai: OEM aur data center team controlled environment mein mil kar repair handle karte hain.

**Participant:** Bohat shukriya sir, ab bohat clear ho gaya.

**Instructor:** You're welcome.

### 19. Disaster Recovery (DR) Site Ki Planning

**Instructor:** Ab maan lijiye humne primary data center implement kar diya aur decide kar liya ke primary location Los Angeles mein hogi. Sarfraz ne pehle ek aur important point raise kiya tha: hamare paas **disaster recovery (DR)** location bhi honi chahiye.

Bilkul honi chahiye. Jab itne servers lag rahe hain, to un mein critical systems bhi honge. Hamein IBM se poochna chahiye ke DR location kahan rakhni hai. Ho sakta hai customer ne pehle se location decide ki ho, ya humse recommendations mangi jayein.

Architect ke taur par hamein blank nahin jana chahiye. Client ko suitable options suggest karne ki preparation honi chahiye. Misaal ke taur par data center provider se pooch sakte hain ke us ki doosri facilities kahan hain aur DR ke liye kaun si site suitable ho sakti hai.

### 20. RTO, RPO aur Disaster Recovery Drills

**Instructor:** Primary DC aur disaster recovery ki discussion mein do important concepts aate hain: **RTO** aur **RPO**. In par hum cloud computing class mein bhi baat kar chuke hain.

RTO aur RPO is baat se related hain ke agar primary data center unavailable ho jaye, to service kitni jaldi restore honi chahiye, aur latest data mein se kitna data recovery ke liye available hoga ya kitna data loss tolerate karna par sakta hai. DR location aur design decide karne ke liye yeh concepts important hain.

Sirf DR site bana dena kaafi nahin. DR ki **drills**, yani recovery tests, bhi hoti hain. Organization ke mutabiq monthly, quarterly ya six-monthly testing ki ja sakti hai. Instructor ne aisi controlled testing ka example diya jahan primary DC ki service intentionally unavailable karke check kiya jata hai ke DR kaam kar raha hai ya nahin.

**Participant:** Yeh to achhi baat hai.

**Instructor:** Bilkul. Hum aisa nahin keh sakte ke disaster aayega to us waqt dekh lenge. Drill se pata chalta hai ke DR environment ke kaun se parts sahi chal rahe hain aur kahan failures hain. Phir jo issues milte hain un ke tickets bante hain aur team un par kaam karti hai.

**Participant:** Right, very clear.

### 21. Abhi Tak Kin Topics Par Detailed Baat Nahin Hui?

**Instructor:** Dekhiye, baat server build se shuru hui thi aur hum complete data-center planning tak aa gaye. Hum approximately aadha ghanta environment ki discussion kar chuke hain, aur abhi tak **operating system install nahin hua**.

Storage, networking, backup tools aur monitoring tools ko bhi abhi detail se discuss nahin kiya. Hum abhi sirf server-side planning ko samajh rahe hain.

**Instructor:** Anil, kya aap hamare saath hain? Koi doubt ya question?

**Participant:** Yes sir. No questions.

**Instructor:** Sarfraz ji?

**Participant:** Nahin sir, aage chalte hain.

### 22. Next Section Ki Taraf: Servers Implement Kaise Honge?

**Instructor:** Ab humne primary DC aur DR location ke bare mein discussion kar li. Class ki ek aur example ke liye assume kar lete hain ke primary data center **Delhi** mein hai aur DR site **Hyderabad** mein. Is tarah hamein local scenario mil jayega jahan hum implementation samajh sakte hain.

Ab agla topic **implementation** hai. Hum dekhenge ke servers ko practically deploy kaise kiya jayega.

---

**Part 3 yahan complete hota hai.** Original transcript ki **line 497** se next discussion start hoti hai: kya 200 physical servers par Windows Server ek ek karke install karna hoga, aur agar har server ka SLA eight hours ho to project time par kaise complete hoga?

> **Source note:** Lecture mein di gayi server quantities, locations, staffing, support period aur DR-drill examples samjhane ke liye hain. Har organization ke liye yeh fixed rules nahin. Recording ke kuch terms unclear hain; unhein bina verification ke naye facts mein convert nahin kiya gaya.
