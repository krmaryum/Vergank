# VMware Training Class — Tafseeli Roman Urdu Transcript

## Part 01: Classroom Discussion, Lab Practice, Datastore Troubleshooting aur Virtual Machines ka Introduction

**Lecture date:** 21 November 2026  
**Source coverage:** Original transcript lines 1–118 (total 682 lines).  
**Tareeqa:** Yeh topic-wise summary nahi, balkay classroom-style tafseeli Roman Urdu tarjuma hai. Instructor ki baat, students ke sawalat, misaalein aur discussion ki original sequence preserve ki gayi hai. Source ke speaker numbers hi use kiye gaye hain. Jahan audio wazeh nahi, wahan andaza lagane ke bajaye note kiya gaya hai.

### 1. Salam-dua aur Class ka Technical Setup (Lines 1–28)

**Speaker 1:** Good morning, everyone.

**Speaker 2:** [Original auto-transcript ke kuch ibtidaai jumlay wazeh nahi hain. Lagta hai speaker kisi software ya page ko open/navigate kar raha hai, database aur scrolling menu ka zikr bhi aata hai, lekin lafz itne clear nahi ke un ka sahi tarjuma kiya ja sake.]

**Speaker 2:** [Urdu mein ek ghair-rasmi guftagu hai, jis ka kuch hissa samajh nahi aa raha.] Screen sab ko visible hai?

**Speaker 1:** Yes sir.

**Speaker 2:** Perfect.

**Speaker 1 (Instructor):** Actually maine screen thori der se share ki, kyun ke mera server abhi power on ho raha tha. Ab woh on ho chuka hai. Main ek dafa is par login kar leta hoon. Okay, okay.

### 2. Pichhli Class ka Review aur Lab Practice (Lines 29–44)

**Speaker 1 (Instructor):** Pichhli class mein humne vCenter ke andar dekha tha ke cluster par HA kaise configure karte hain, DRS kaise configure karte hain, vMotion kaise use karte hain, aur affinity rules kaise create karte hain. Theek hai? Aaj ka session start karne se pehle yeh bataiye ke aap sab ki practice kaisi chal rahi hai?

**Speaker 3:** Sir, meri to bilkul practice nahi ho pa rahi.

**Speaker 1 (Instructor):** Aur Khalid, sorry. Ho sakta hai aap ki practice na ho paane mein kuch hadd tak meri bhi wajah ho. Aap ne mujh se multiple times questions poochhe aur servers ki details bheji theen. Aaj hum class mein un details ko discuss kar lenge.

**Speaker 3:** Bohat bohat shukriya.

**Speaker 1 (Instructor):** Bilkul, bilkul. Actually mujhe minimum time bhi nahi mil raha tha, is liye shayad main aap ko reply hi nahi kar paaya. Khair, aaj class mein check kar lete hain ke lab ke liye minimum configuration kya honi chahiye, taake aap apni lab practice kar sakein. Right?

**Speaker 3:** Bohat shukriya, sir.

**Speaker 1 (Instructor):** Baqi members batayein, practice chal rahi hai?

**Ek participant:** Ji, main lab kar raha hoon aur class ke sessions ki practice bhi kar raha hoon.

**Goutham (Guest):** Sir, mera ek doubt hai. Jab hum host ya VM ke liye 500 GB ya 4 TB disk specify karte hain, to KR lab mein mujhe roughly 200 GB free space nazar aa raha tha. Phir bhi lab mein configuration ho gayi. Yeh kaise possible hai?

**Speaker 1 (Instructor):** Ji, aaram se ho sakta hai. Jab hum yeh labs karte hain, to takreeban 150 GB space ke andar poori lab ho sakti hai. Jo 4,000 GB ya 4 TB disk space hum specify kar rahe hain, woh is example mein virtual allocation hai. Hum physically poori 4 TB space use nahi kar rahe. Is liye aap lab kar sakte hain.

**Participant:** Okay, okay. Sure sir.

### 3. ESXi Host Add Karne ke Baad Datastore Kyun Nahi Dikhta? (Lines 45–72)

**Participant:** Sir, ek aur doubt tha. Jab hum ESXi host ko vCenter mein add karte hain, to host add ho jaata hai, lekin Datastore section mein storage nazar nahi aa rahi thi. Main ne host par ek additional hard disk lagayi, us ke baad disk nazar aa gayi. Aisa kyun hua?

**Speaker 1 (Instructor):** Okay. Mere khayal mein yeh VMware Workstation ka issue hai. Kabhi kabhi jab ESXi host ko vCenter ka member banate hain, to aisa ho jaata hai. Main abhi vCenter Server console kholta hoon, cluster select karta hoon aur Datastores check karta hoon. Yahan mere chaaron ESXi hosts ka datastore information show ho raha hai.

**Speaker 1 (Instructor):** Lekin kai baar yeh information show nahi hoti. Aap samajhte hain shayad hum se koi mistake ho gayi. Meri observation mein zaroori nahi ke yeh aap ki mistake ho. VMware Workstation ke nested lab mein bhi aisa dekhne ko mil sakta hai.

**Speaker 1 (Instructor):** Is surat mein mere paas do approaches hain: ya to ESXi host ko reinstall kar dein, ya usay reset karein. Reset ka matlab hai host ka DCUI, yani Direct Console User Interface, open karna aur us ki settings check karna. Main VMware Workstation mein dikha deta hoon.

**Speaker 1 (Instructor):** Jis ESXi host ka datastore show nahi ho raha us ki console open karein. Screen par 'Press F2 for DCUI' nazar aayega. F2 press karke login karein.

**Speaker 1 (Instructor):** Neeche 'Reset System Configuration' ka option hota hai. Agar isay select karke F11 se confirm karein to ESXi host ki configurations reset ho jaati hain. Aap ko host dobara configure karna padega. Jo additional settings ki theen woh bhi reset ho jayengi.

**Speaker 1 (Instructor):** Yeh kuch us tarah hai jaise mobile phone ko hard reset karte hain. Mobile par kabhi poochha jaata hai ke data rakhna hai ya nahi. Yahan reset ko ek clean configuration ki tarah samjhein. Phir ESXi host ko dobara IP address dein, settings karein aur, mere proposed lab procedure ke mutabiq, disk visible ho sakti hai.

**Participant:** Achha, to aap keh rahe hain ke yeh VMware Workstation ka issue ho sakta hai, hamari taraf ki mistake zaroori nahi?

**Speaker 1 (Instructor):** Ji. Main ne Workstation mein aisa dekha hai aur feedback bhi diya tha. Abhi tak mujhe is ke liye update nazar nahi aaya. Workstation 17 family se yeh behavior main ne dekha, jabke version 16 par mujhe aisa issue nahi mila. Help > About mein ab aap ko 25 ya 26 family ka version nazar aa sakta hai, lekin meri observation 17 se shuru hui thi.

**Speaker 1 (Instructor):** Aap ne jab additional hard disk lagayi thi, woh disk nazar aa gayi, lekin purani expected drive show nahi ho rahi thi, sahi?

**Participant:** Ji, additional disk nazar aa gayi thi.

**Speaker 1 (Instructor):** Haan ji, main isi case ki baat kar raha hoon.

> **Editor ki safety note — instructor ki guftagu ka hissa nahi:** 'Reset System Configuration' disruptive aur destructive operation hai. Missing datastore ke liye pehla step nahi hona chahiye. Pehle controller, storage device detection, VMFS datastore creation/mount, rescan aur configuration check karein. Kisi specific Workstation version ko issue ki proven wajah samajhna bhi bina verification ke theek nahi.

### 4. Online VMware Labs aur Certification Exams (Lines 73–97)

**Speaker 1 (Instructor):** Ab aaj hum sab se pehle Virtual Machine ka chapter start karenge.

**Anshul Saini:** Sir, online VMware lab bhi hai. Kya hum wahan practice kar sakte hain? Agar agle hafte KR lab ka access timing ki wajah se mushkil ho to online labs use ho sakti hain?

**Speaker 1 (Instructor):** Ji ji, bilkul try kar sakte hain. Lekin un ki limitations pehle samajh lein. Yeh VMware virtual labs hain.

**Speaker 1 (Instructor):** Microsoft ke bhi is qisam ke labs hote hain. Un mein fundamentals practice kiye ja sakte hain. VMware ne bhi milta-julta tareeqa use kiya. Lekin guided web labs mein har button aur har click available nahi hota.

**Speaker 1 (Instructor):** Example ke taur par, agar lab Storage Deployment ke liye design ki gayi hai, to us se related steps kaam karenge. Extra options par click karein ge to shayad woh kaam na karein. Yeh ek tarah ka simulated ya restricted webpage hota hai jahan prescribed tasks hi kar sakte hain.

**Speaker 1 (Instructor):** Is mein zaroori nahi ke aap complete fresh ESXi host install kar sakein, kisi bhi service ko enable/disable kar sakein, ya saari settings freely use kar sakein. Aap ke paas exercise ke mutabiq limited access hota hai.

**Speaker 1 (Instructor):** Misaal ke taur par aap Virtual Machine creation ki lab kar rahe hain. Storage par click to ho sakta hai, magar aage detail na dikhe, ya dikhe lekin aage kisi control ko use na kar sakein. Yeh un labs ki limitation ho sakti hai.

**Participant:** Okay. Kya certification exam mein bhi isi tarah tasks test karte hain?

**Speaker 1 (Instructor):** Pearson VUE bohat si global certification exams conduct karta hai. Microsoft, networking, VMware aur doosre certifications ke exams testing providers ke zariye hote hain. Pehle Pearson VUE aur Prometric dono naam sunne ko milte thay.

**Speaker 1 (Instructor):** Scenario-based exam mein mumkin hai aap ko simulated interface mile, jahan koi service fail ho aur aap ko troubleshooting karni ho. Us interface mein sirf relevant options clickable hon, har cheez available na ho.

**Participants:** Okay, samajh aa gaya. Ji sir.

> **Editor ka note:** Exam provider aur exam simulations ka format certification ke mutabiq change hota hai. Yahan instructor ki classroom explanation preserve ki gayi hai; isay har exam ka universal rule na samjhein.

### 5. Virtual Machine Chapter ka Introduction (Lines 98–118)

**Speaker 1 (Instructor):** Aaj ka chapter bohat interesting aur important hai: Virtual Machine. VM create karne se pehle pichhli class ka kaam yaad kar lete hain.

**Participant:** Sir, aap ki voice lag ho rahi hai, break ho rahi hai.

**Speaker 1 (Instructor):** Shayad network ka issue hai. Main network switch karke check karta hoon. Hello, hello. Ab voice sahee aa rahi hai?

**Participants:** Ji sir, ab aa rahi hai.

**Speaker 1 (Instructor):** Mera core network aaj kuch issue kar raha hai. Kal raat 11–12 baje tak theek chal raha tha. Aaj subah se problem hai. Ek baar cross-check kar leta hoon. Chaliye continue karte hain.

**Speaker 1 (Instructor):** Last class mein hum ne software-based data center create kiya tha. Kya screen visible hai sab ko?

**Participants:** Ji sir, screen visible hai.

**Speaker 1 (Instructor):** Data center banane ke baad hum ne apne ESXi hosts us mein add kiye thay. Saath mein cluster bhi banaya tha. Cluster kyun banaya? Ek reason DRS use karna tha, jisay hum ne pichhli class mein dekha.

**Speaker 1 (Instructor):** Misaal ke taur par agar kisi ESXi host par utilization bohat high ho jaye, aur us par chalne wali kuch virtual machines ko sufficient CPU ya memory na mil rahi ho, to DRS cluster ke andar munasib virtual machines ko doosre host par move karne mein madad karta hai jahan resources available hon.

**Speaker 1 (Instructor):** Hum ne High Availability bhi dekhi. Agar koi ESXi host power failure ya doosre issue ki wajah se down ho jaye, to HA available cluster hosts par affected virtual machines ko dobara run karne mein madad deta hai.

**Speaker 1 (Instructor):** Yeh cluster ke bohat useful features hain. Isi liye hum ne cluster create kiya. Saath hi ek VMware storage solution banaya tha jise vSAN kehte hain. Pehle hum network-attached ya SAN storage use kar rahe thay. vSAN bhi VMware ki ek capability hai.

**Speaker 1 (Instructor):** Ab agla step hai apne VMware infrastructure ke andar virtual servers create karna. CPU aur memory ke liye ESXi hosts hain, storage ke options bhi hain. Ab samajhna hai ke virtual machine create aur run karne ke liye kin resources ki zaroorat hoti hai.

> **Tarjume ki boundary:** Yeh Part 01 original transcript ki line 118 par khatam hota hai. VM resources aur distributed switch ki demonstration aage source mein maujood hain. Is file ko poori lecture ka complete translation claim nahi kiya gaya.
