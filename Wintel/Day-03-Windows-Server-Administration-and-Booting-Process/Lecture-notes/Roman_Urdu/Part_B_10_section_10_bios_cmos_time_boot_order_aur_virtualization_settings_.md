# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 10 — BIOS, CMOS time, boot order aur virtualization settings (Source B:180–210)

**Instructor (B:180–184):** BIOS ko main firmware chip aur mini operating system ke taur par describe kar raha tha. Yeh hardware settings aur date/time se related information deta hai. Agar CMOS battery fail ho aur aap replace karein to instructor ke mutabiq BIOS setup mein date/time update karke save/restart karne se clock related settings theek hoti hain. Woh keh rahe hain ke CMOS ko directly edit karne ke bajaye BIOS interface use karte hain.

**Instructor (B:185–191):** Interview mein poocha ja sakta hai: "CMOS battery replace kar di, ab date/time kaise update karoge?" Expected classroom reply hai: "BIOS/firmware setup open karke correct date/time set karenge, changes save karke restart karenge." Instructor yeh bhi kehte hain ke OEMs ke paas low-level hardware access hota hai. Is explanation ko original lecture ke taur par samjhein; hardware-specific clarification alag technical note mein di gayi hai.

**Instructor (B:192–200):** BIOS setup mein ek aur bohat important setting **boot device priority** hai. Aap decide karte hain pehla boot device USB hoga, SSD/hard disk hoga, ya koi aur option. Example: agar installed OS corrupt hai ya naya OS install karna hai, bootable USB insert karte hain aur boot order mein USB ko prefer karte hain. Taake restart par system hard disk ke corrupt OS ki jagah USB ke boot files se start ho.

**Instructor (B:201–207):** Teesri important cheez **Virtualization Technology (VT)** hai. Hyper-V, VMware Workstation, ESXi ya doosre virtualization use cases ke liye CPU virtualization settings ka enabled hona zaroori ho sakta hai. Har laptop/server model ke BIOS/UEFI menus alag hote hain, is liye apne model ka documentation check karein. Instructor Windows Task Manager khol kar **Performance → CPU → Virtualization: Enabled** dikhate hain.

**Instructor (B:208–210):** Virtualization enabled hone ki wajah se woh apni machine par virtual labs chala rahe hain. Agar disabled hoti to firmware settings change karni padtin. Instructor ek baar jumle mein "virtualization" keh dete hain, phir correct karke bolte hain ke settings BIOS mein stored hoti hain. Ab security-related agla topic aata hai.

