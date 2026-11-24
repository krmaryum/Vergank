# Interview Sawal aur Jawab: Windows Server 2019 Installation

**Zabaan (Language):** [English](INTERVIEW-QA.md) | Roman Urdu  ·  Wapas [guide](README.roman-urdu.md) par

Is lab par mabni 25 beginner level sawal jo help desk, junior sysadmin ya IT support interview mein poochay ja sakte hain.

**Practice kaise karein:** Jawab chhupa lein, apna jawab **buland awaaz mein** bolein, phir milayen. Interviewers ko chhote, saaf jawab pasand hain, aur saath ek asli misaal ("Apne lab mein maine...").

> **Note:** Interview aam tor par English mein hota hai, is liye technical alfaaz English mein hi rakhe gaye hain. English jawab [INTERVIEW-QA.md](INTERVIEW-QA.md) mein hain.

## Fehrist

- [Windows Server 2019 ki buniyadi baatein](#windows-server-2019-ki-buniyadi-baatein) (Q1 se Q7)
- [Installation](#installation) (Q8 se Q13)
- [Virtual machines aur VMware](#virtual-machines-aur-vmware) (Q14 se Q20)
- [Firmware aur boot](#firmware-aur-boot) (Q21 se Q22)
- [Installation ke baad](#installation-ke-baad) (Q23 se Q25)

---

## Windows Server 2019 ki buniyadi baatein

### Q1. Windows Server kya hai, aur yeh Windows 10 se kaise alag hai?
**Jawab:** Windows Server Microsoft ka **servers** ke liye operating system hai: aise computers jo doosre computers ko services dete hain, jaise login, file sharing, websites ya DNS. Windows 10 ek **client** OS hai jo ek shakhs ke rozana kaam ke liye hai. Server mein **roles** (jaise Active Directory, DNS, DHCP, File Services) hote hain, yeh ek waqt mein bohat se users ko support karta hai, aur is ki licensing alag hoti hai.

### Q2. Windows Server 2019 ki kaun si editions hain?
**Jawab:** Main editions **Essentials** (chhote business, 25 users tak), **Standard**, aur **Datacenter** hain. Standard aur Datacenter ke core features ek jaise hain; Datacenter mein advanced features aur unlimited virtualization rights hain.

### Q3. Standard aur Datacenter mein kya farq hai?
**Jawab:** **Standard** license se aap licensed host par **2** Windows Server VMs chala sakte hain. **Datacenter** **unlimited** Windows Server VMs ki ijazat deta hai aur **Storage Spaces Direct**, **Shielded VMs** aur poori **Storage Replica** jaise features deta hai. Datacenter un jagahon ke liye hai jahan bohat zyada virtualization ho. *Apne lab mein maine Datacenter Evaluation install kiya taake har feature try kar sakoon.*

### Q4. Server Core aur Desktop Experience mein kya farq hai?
**Jawab:** **Desktop Experience** mein poora graphical desktop hota hai (Start menu, File Explorer, Server Manager). **Server Core** mein **desktop nahin**, sirf command window hoti hai; isay PowerShell, `sconfig`, ya kisi doosre computer se remotely manage karte hain. Server Core kam disk aur RAM leta hai, kam updates chahiye, aur is ka **attack surface chhota** hai (hack karne ke liye kam cheezein). Server 2019 mein yeh setup ke dauran chuna jaata hai, aur baad mein reinstall ke baghair badla nahin ja sakta.

### Q5. Company Server Core kyun chunegi?
**Jawab:** Yeh **zyada mehfooz** hai (attack ke liye kam software), updates ke liye **kam restart** chahiye, aur **kam resources** leta hai. Zyada tar servers waise bhi remotely manage hote hain, is liye desktop ki aksar zaroorat nahin hoti.

### Q6. Windows Server 2019 ki minimum hardware requirements kya hain?
**Jawab:** **1.4 GHz 64-bit** processor, Server Core ke liye **512 MB RAM** (Desktop Experience ke liye **2 GB**), aur **32 GB** disk space. Amli tor par is se zyada dena chahiye. *Apne lab mein maine 2 cores, 4 GB RAM aur 80 GB disk di.*

### Q7. Evaluation version kya hai, aur kitne din chalta hai?
**Jawab:** Yeh poora product hai, free try karne ke liye, **180 din** tak. Isay product key ke baghair install karte hain. 180 din ke baad yeh activate hone tak baar baar shut down hona shuru kar deta hai. Labs aur testing ke liye behtareen hai. Valid key se evaluation ko licensed version mein convert kiya ja sakta hai.

---

## Installation

### Q8. ISO file kya hai?
**Jawab:** Ek file jo **DVD ki hoobahoo image** hai. VM mein ISO ko virtual CD/DVD drive se jorte hain aur VM us se aise boot karti hai jaise asli disc ho.

### Q9. Custom aur Upgrade installation mein kya farq hai?
**Jawab:** **Upgrade** disk par pehle se maujood purani Windows ki files, settings aur apps rakhta hai. **Custom (clean install)** khali ya format ki hui partition par nayi copy install karta hai. Naye server ke liye **Custom** chunte hain.

### Q10. Disk select karne wali screen par "Unallocated Space" ka kya matlab hai?
**Jawab:** Disk par **koi partition nahin**: khali hai aur format nahin hui. Isay select karke Next dabane par Setup khud zaroori partitions (system, recovery aur main Windows partition) banata hai aur unhein **NTFS** se format karta hai.

### Q11. Administrator account ke password ke kya qawaid hain?
**Jawab:** Default mein Windows Server **complex password** maangta hai: kam az kam **8 characters**, aur **chaar mein se 3 groups** ke characters: bare huroof, chhote huroof, numbers, symbols. Is mein user name bhi nahin hona chahiye.

### Q12. Server ko default time zone ke saath kyun nahin chhorna chahiye?
**Jawab:** Setup default mein **Pacific Time** rakhta hai. Ghalat time zone se logs mein ghalat waqt aata hai, aur domain mein **agar ghariyon mein 5 minute se zyada farq ho to Kerberos authentication fail ho jaati hai**. *Apne lab mein time zone theek karne tak VM host se 2 ghante peeche thi.*

### Q13. VMware VM mein Ctrl+Alt+Del dabane se host ka menu khulta hai. Kyun, aur kya karein?
**Jawab:** **Host** OS hamesha Ctrl+Alt+Del pakar leta hai. VMware Workstation mein **Ctrl+Alt+Insert** dabayen, ya **VM > Send Ctrl+Alt+Del** use karein.

---

## Virtual machines aur VMware

### Q14. Virtual machine kya hai?
**Jawab:** Ek **software computer** jo asli computer par chalta hai. Is ka apna virtual CPU, memory, disk aur network card hota hai, aur yeh apna operating system chalata hai. Ek physical machine par kai VMs ek doosre se alag chal sakti hain.

### Q15. Hypervisor kya hai? Is ki do qismein kaun si hain?
**Jawab:** Hypervisor woh software hai jo VMs banata aur chalata hai.
- **Type 1 (bare-metal)** seedha hardware par chalta hai, neeche koi OS nahin. Misaal: **VMware ESXi**, **Microsoft Hyper-V**. Data centers mein use hota hai.
- **Type 2 (hosted)** aam OS ke upar ek application ki tarah chalta hai. Misaal: **VMware Workstation**, **VirtualBox**. Labs aur testing ke liye.

### Q16. Host aur guest mein kya farq hai?
**Jawab:** **Host** woh asli computer hai jis par hypervisor chal raha hai. **Guest** VM ke andar chalne wala OS hai. *Mere lab mein: host = Windows 10 Pro, guest = Windows Server 2019.*

### Q17. Bridged, NAT aur Host-only networking samjhayen.
**Jawab:**
- **Bridged:** VM seedha physical network se juri hoti hai aur asli router se **apna IP** leti hai, network par ek aur PC ki tarah.
- **NAT:** VM **host ka IP address share** karti hai. Internet tak pohanch sakti hai, lekin doosre devices aasani se us tak nahin pohanch sakte.
- **Host-only:** VM sirf **host** aur doosri host-only VMs se baat kar sakti hai. Internet nahin.

*Maine Bridged use kiya kyun ke server tak network ke doosre computers ki pohanch honi chahiye.*

### Q18. VMware Tools kya hai, aur kyun install karein?
**Jawab:** Guest OS ke liye **drivers aur services** ka package. Is se behtar video (screen resize), smooth mouse, host aur guest ke darmiyan copy/paste, behtar network aur disk performance, aur **time sync** milta hai. VMware VM mein hamesha install karna chahiye.

### Q19. Thin-provisioned disk aur split disk mein kya farq hai?
**Jawab:** **Thin provisioning** ka matlab hai disk file **chhoti shuru hoti hai aur data likhne ke saath barhti hai**, maximum size (maslan 80 GB) tak. **Split** ka matlab hai disk ek bari file ke bajaye **kai chhoti files** mein rakhi jaati hai, jis se copy aur move karna aasaan hai. Workstation mein disk dono ho sakti hai.

### Q20. Snapshot kya hai, aur kya yeh backup hai?
**Jawab:** Snapshot **VM ki ek waqt ki haalat** save karta hai taake aap baad mein wapas ja sakein. Yeh asli backup **nahin** hai, kyun ke yeh original disk files par depend karta hai: agar woh gum ya kharab ho jaayen to snapshot bhi bekaar hai. Risky tabdeeli se pehle snapshot behtareen hai, lekin isay lamba arsa nahin rakhna chahiye.

---

## Firmware aur boot

### Q21. BIOS aur UEFI mein kya farq hai?
**Jawab:** Dono **firmware** hain jo OS se pehle computer start karte hain.
- **BIOS** (Legacy) purana hai, **MBR** disks use karta hai (max **2 TB**, max 4 primary partitions), aur Secure Boot nahin.
- **UEFI** naya hai, **GPT** disks use karta hai (2 TB se kahin bari, Windows mein 128 partitions tak), tez boot karta hai, aur **Secure Boot** support karta hai jo na-qabil-e-aitbaar boot software ko rokta hai.

Jadeed servers aur Windows 11 UEFI use karte hain.

### Q22. Aap ki VM Windows Setup ke bajaye UEFI Boot Manager dikhati hai. Kya karenge?
**Jawab:** UEFI mein Windows ISO "Press any key to boot from CD or DVD" ke liye sirf chand seconds rukti hai. Agar reh jaaye to VM Boot Manager par aa jaati hai. Hal: VM restart karein, **jaldi andar click karke koi key dabayen**; ya **Power On to Firmware** use karke CD/DVD chunein; ya **OS install karne se pehle** VM Settings > Options > Advanced mein firmware **BIOS** kar dein. *Apne lab mein maine BIOS kiya aur Setup foran start ho gaya.* Install ke baad firmware kabhi na badlein, warna VM boot nahin hogi.

---

## Installation ke baad

### Q23. Server Manager kya hai?
**Jawab:** Windows Server ka main **graphical management console**. Yeh login par khulta hai aur is se aap **roles aur features** add karte hain, events aur services dekhte hain, local server configure karte hain (naam, IP, updates), aur doosre servers manage karte hain.

### Q24. Role aur feature mein kya farq hai?
**Jawab:** **Role** server ka doosron ke liye main kaam hai, jaise **AD DS**, **DNS**, **DHCP**, **File and Storage Services** ya **Web Server (IIS)**. **Feature** madadgar tool hai, jaise **.NET Framework**, **Windows Server Backup** ya **Telnet Client**. Dono Server Manager mein **Add Roles and Features** se (ya PowerShell mein `Install-WindowsFeature` se) add hote hain.

### Q25. Naya server install karne ke baad sab se pehle kya configure karte hain?
**Jawab:**
1. **VMware Tools** install karein (agar VMware VM hai) ya doosre drivers.
2. Sahi **time zone** aur waqt set karein.
3. Computer ka **naam** maani-khez rakhein.
4. **Static IP address** aur sahi **DNS** settings dein.
5. **Windows Update** chalayen.
6. Roles add karne se pehle **snapshot** ya backup lein.
7. Phir roles add karein, maslan domain join karein ya domain controller banayen.

---

**Bonus sawal:** *Windows Server 2019 ki support kab khatam hogi?*
Mainstream support **9 January 2024** ko khatam hui. Extended support (sirf security updates) **9 January 2029** tak hai. Server 2019 ek **Long-Term Servicing Channel (LTSC)** release hai, aur Windows 10 version 1809 wale code base par bana hai.

**Bonus sawal 2:** *Windows Admin Center kya hai?*
Microsoft ka free, **browser-based** management tool. Isay ek dafa server ya PC par install karte hain, phir web browser se kai servers manage karte hain. Yeh Server Manager ka jadeed saathi hai. Server 2019 ka Server Manager is ka pop-up dikhata hai; "Don't show this message again" tick karna bilkul theek hai.
