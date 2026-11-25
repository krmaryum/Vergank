# Interview Sawal aur Jawab: Windows Server 2022 Installation

**Zabaan (Language):** [English](INTERVIEW-QA.md) | Roman Urdu  ·  Wapas [guide](README.roman-urdu.md) par

25 beginner level sawal jo help desk, junior sysadmin ya IT support interview mein is lab ki buniyad par pooche ja sakte hain. VM ki aam buniyadi baatein [2019 Q&A](../WS2019/INTERVIEW-QA.roman-urdu.md) mein bhi hain; yeh set **2022 mein kya naya hai** aur is lab ke steps par focus karta hai.

**Practice kaise karein:** Jawab chhupa lein, apna jawab **buland awaaz** mein bolein, phir milayen. Interviewer chhota, saaf jawab pasand karte hain, saath ek asli misaal ("Meri lab mein, maine...").

## Fehrist

- [Windows Server 2022 ki buniyadi baatein](#windows-server-2022-ki-buniyadi-baatein) (Q1 se Q8)
- [Installation](#installation) (Q9 se Q15)
- [Virtual machines aur VMware](#virtual-machines-aur-vmware) (Q16 se Q21)
- [Installation ke baad](#installation-ke-baad) (Q22 se Q25)

---

## Windows Server 2022 ki buniyadi baatein

### Q1. Windows Server 2022 kab release hua, aur kab tak support milegi?
**Jawab:** Yeh **August 2021** mein release hua (build 20348). Yeh **Long-Term Servicing Channel (LTSC)** release hai, yaani 10 saal ki support: **mainstream support October 2026 mein khatam** hui, aur **extended support** (sirf security updates) **October 2031** tak hai.

### Q2. Windows Server 2022 ki kaun si editions hain?
**Jawab:** **Standard**, **Datacenter**, aur **Datacenter: Azure Edition** (Microsoft Azure ya Azure Stack HCI par chalane ke liye). Chhote kaarobar ke liye **Essentials** bhi hai, jo sirf naye hardware ke saath bikta hai. *Meri lab mein maine Standard (Desktop Experience) install kiya.*

### Q3. Standard aur Datacenter mein kya farq hai?
**Jawab:** Dono ke core features ek jaise hain. **Standard** license licensed host par **2** Windows Server VMs ki ijazat deta hai. **Datacenter** **be-had (unlimited)** VMs deta hai aur **Storage Spaces Direct**, **Shielded VMs** aur **Software-Defined Networking** jaise features add karta hai. Standard kam virtualization ya physical servers ke liye; Datacenter bari virtualization wale data centers ke liye.

### Q4. Windows Server 2022 ke kuch naye features batayen.
**Jawab:**
- **Secured-core server**: hardware security (TPM 2.0, Secure Boot, virtualization-based security) se firmware hamlon se bachata hai.
- **TLS 1.3** default mein on, mehfooz network connections ke liye.
- **DNS over HTTPS (DoH)** client, taake DNS lookups encrypt ho sakein.
- File sharing ke liye **SMB AES-256 encryption**, aur **SMB over QUIC** (Azure Edition) baghair VPN ke internet par mehfooz file access ke liye.
- Internet Explorer ki jagah **Microsoft Edge** built in.
- Behtar **Azure hybrid** tools (Azure Arc, Windows Admin Center).

### Q5. Server Core aur Desktop Experience mein kya farq hai?
**Jawab:** **Desktop Experience** mein poora graphical desktop hai (Start menu, Server Manager, File Explorer). **Server Core** mein **desktop nahin**, sirf command window; ise PowerShell, `sconfig`, ya door se manage karte hain. Server Core chhota hai, kam updates chahiye, aur **attack surface chhota** hai. Setup ke waqt chunte hain, aur baad mein baghair reinstall ke badal nahin sakte.

### Q6. Windows Server 2022 ki kam az kam hardware zaroorat kya hai?
**Jawab:** **1.4 GHz 64-bit** processor, Server Core ke liye **512 MB RAM** (Desktop Experience ke liye **2 GB**), aur **32 GB** disk. Amli tor par zyada dein. *Meri lab mein: 2 cores, taqreeban 4 GB RAM, 80 GB disk.*

### Q7. Kaise pata chalega ke ISO evaluation version hai?
**Jawab:** Setup mein edition ke naamon mein lafz **"Evaluation"** hota hai, maslan *Windows Server 2022 Standard Evaluation*. Evaluation baghair key ke **180 din** chalti hai. *Meri lab mein naamon mein "Evaluation" nahin tha, is liye mujhe pata chala ke yeh aam ISO hai jise activate karne ke liye product key chahiye.*

### Q8. Agar Windows Server activate na ho to kya hota hai?
**Jawab:** Phir bhi install hokar chalta hai, aur roles bhi chalte hain, lekin **"Activate Windows"** watermark nazar aata hai, kuch personalization settings band hoti hain, aur yeh **sahi tarah licensed nahin** hota. Production mein server hamesha valid license se activate hona chahiye.

---

## Installation

### Q9. Aap ne VMware mein "I will install the operating system later" kyun chuna?
**Jawab:** Taake VMware **Easy Install** na chalaye, jo Setup ke sawalon ke jawab khud de deta hai. Lab mein main har Setup screen khud dekhna chahta tha. ISO maine baad mein **Customize Hardware** mein lagayi.

### Q10. Aap ne firmware BIOS kyun kiya, aur kab badalna mehfooz hai?
**Jawab:** **UEFI** ke saath Windows ISO "Press any key to boot from CD or DVD" ke liye sirf chand second rukti hai. Chook jaayen to VM **Boot Manager** par chali jaati hai. Meri 2019 lab mein yahi hua tha. **BIOS** ISO foran boot karta hai. Badalna **sirf Windows install karne se pehle** mehfooz hai, kyun ke BIOS aur UEFI disk ka alag layout istemal karte hain (**MBR** vs **GPT**); baad mein badalne se Windows boot nahin hoti. *Apni 2022 lab mein maine pehli boot se pehle BIOS kiya aur koi masla nahin aaya.*

### Q11. Custom aur Upgrade installation mein kya farq hai?
**Jawab:** **Upgrade** disk par purani Windows ki files, settings aur apps rakhta hai. **Custom** khaali ya format shuda disk par saaf install hai. Naye server ke liye **Custom** chunte hain.

### Q12. Disk screen par "Unallocated Space" ka kya matlab hai?
**Jawab:** Disk par abhi **koi partition nahin**. Select karke Next dabayen to Setup zaroori partitions khud banata hai aur unhen **NTFS** se format kar deta hai.

### Q13. Virtual disk NVMe hai. Kya driver load karna parega?
**Jawab:** Nahin. Windows Server 2022 mein **NVMe driver pehle se maujood** hai, is liye disk Setup mein foran nazar aati hai. **Load driver** sirf un disk controllers ke liye hai jinhen Windows nahin pehchanti.

### Q14. Administrator account ke password ke usool kya hain?
**Jawab:** **Complex password**: kam az kam **8 characters**, **4 mein se 3 groups** ke characters (bare huroof, chhote huroof, numbers, symbols), aur is mein user ka naam nahin ho sakta.

### Q15. Setup ke dauran VM restart hoti hai aur "Press any key to boot from CD or DVD" aata hai. Aap kya karenge?
**Jawab:** **Kuch nahin.** Key na dabayen. Setup hard disk se aage chalna chahta hai. Key dabane se ISO dobara boot hogi aur Setup shuru se chalega.

---

## Virtual machines aur VMware

### Q16. VM ko D: par kyun rakha, default location par kyun nahin?
**Jawab:** Default location `C:` par **OneDrive** ke andar hai. OneDrive har tabdeeli cloud par sync karna chahta hai, aur VM files bari aur har waqt badalti hain, is liye sync slow hai aur VM **kharab** kar sakta hai. `D:` par jagah bhi bohat zyada thi. *Maine `D:\VMs\WinSRV-2022` mein rakhi.*

### Q17. "Split virtual disk into multiple files" kya karta hai?
**Jawab:** Virtual disk ko ek bari file ki jagah kai chhoti files mein rakhta hai. Chhoti files **copy, move aur backup** karna aasaan hai. Disk **thin** bhi hai: chhoti shuru hoti hai aur data likhne ke saath barhti hai.

### Q18. Aap ne Bridged networking kyun istemal ki?
**Jawab:** **Bridged** VM ko seedha asli network par rakhta hai, **apne IP address** ke saath, ek aur PC ki tarah. Server tak doosre computers ki pohanch honi chahiye. **NAT** VM ko host ke IP ke peeche chhupata hai, aur **Host-only** mein bahar ka network hota hi nahin.

### Q19. VMware Tools kya hai, aur kaise pata chalega ke kaam kar raha hai?
**Jawab:** Guest ke liye **drivers aur services** ka package: behtar display, smooth mouse, copy/paste, behtar network aur disk performance, aur time sync. Kaam ka pata tab chalta hai jab **screen window ke saath resize** ho, mouse aazadi se chale, aur menu mein **Reinstall VMware Tools** nazar aaye. *Meri lab mein install ke baad chhoti screen poori window bhar gayi.*

### Q20. VMware Tools: Typical ya Complete?
**Jawab:** **Typical** sirf woh install karta hai jo maujooda VMware product (Workstation) ko chahiye. **Complete** saare features install karta hai, agar VM kisi aur VMware product jaise **ESXi** par jaaye. *Maine Complete chuna.*

### Q21. VMware mein peeli "I Finished Installing" patti kya hai?
**Jawab:** VMware ki yaad dihaani jo tab aati hai jab aap ne OS baad mein install karna chuna ho. **I Finished Installing** dabane se VMware ko pata chalta hai ke install mukammal hai aur patti hat jaati hai. VM mein kuch nahin badalta.

---

## Installation ke baad

### Q22. Server Manager mein "Services" par laal number hai. Kya kuch toota hai?
**Jawab:** Zaroori nahin. Yeh un services ko ginta hai jo **Automatic** par hain lekin **chal nahin rahin**. Naye server par yeh aam hai: kuch services der se start hoti hain (*Delayed Start*) ya sirf zaroorat par (*trigger start*), aur kuch update services kaam khatam karke ruk jaati hain. Main **Services** par click karke dekhta hoon kaun si hain, chand minute baad refresh karta hoon, aur sirf zaroori service ko start karta hoon.

### Q23. Ghari theek lag rahi ho tab bhi time zone kyun check karein?
**Jawab:** Ghari aaj theek lag sakti hai lekin zone ghalat ho sakta hai, ya **daylight saving** ki tabdeeli miss ho sakti hai. Active Directory mein **Kerberos** clocks mein **5 minute** se zyada farq par fail ho jaata hai. Maine **(UTC-06:00) Central Time (US & Canada)** rakha, *Central America* nahin, jis mein daylight saving nahin hoti.

### Q24. Role aur feature mein kya farq hai?
**Jawab:** **Role** server ka doosron ke liye bara kaam hai, jaise **AD DS**, **DNS**, **DHCP** ya **IIS**. **Feature** madadgaar tool hai, jaise **.NET Framework** ya **Windows Server Backup**. Dono Server Manager mein **Add Roles and Features** se, ya PowerShell mein `Install-WindowsFeature` se add hote hain.

### Q25. Naya server install karne ke baad pehle kya configure karte hain?
**Jawab:**
1. **VMware Tools** (ya hardware drivers) install karein.
2. **Time zone** check karein.
3. Server ka **naam badlein**.
4. **Static IP** aur DNS set karein.
5. **Windows Update** chalayen.
6. Windows **activate** karein (agar evaluation nahin).
7. **Snapshot** ya backup lein, phir roles add karein.
