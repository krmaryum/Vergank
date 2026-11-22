# Day 03 Part A — VMware Tools verification, performance and student questions

**Original-source reference:** A:79–128.

**Instructor (A:79–83):** Reboot ke baad display ka result dekhiye. Ab screen poori fit ho rahi hai, aur jab main VMware Workstation ki window ko chhota karta hoon to guest OS apna resolution adjust kar raha hai. Student se poochta hoon ke pehle virtualization labs banaye hain? Jawab aata hai ke Linux aur Windows ki VMs VirtualBox mein banayi hain, VMware mein nahin. Main kehta hoon ke jis tool se familiarity hoti hai, insaan use hi sabse convenient samajhta hai. Lekin Workstation mein extra integration aur networking options hain.

**Student (A:84):** Sir, kuch log kehte hain VMware heavy hai aur VirtualBox halka. Yeh baat kya hai?

**Instructor (A:85–92):** Main samjhata hoon ke zyada features hone ki wajah se program ki services aur resource utilization alag ho sakti hai. Task Manager se CPU aur RAM check ki ja sakti hai. Purane Windows XP aur Windows Server 2003 ke din yaad karein: us waqt 64 MB, 128 MB, 256 MB, ya 512 MB RAM ki baat hoti thi. Aaj hardware aur applications ki requirements bohat badh chuki hain. Mobile phones mein bhi kai gigabytes RAM aam hai. Is se example milta hai ke software functionality ka infrastructure par asar hota hai.

**Instructor (A:93–103):** Ab Windows Server ke Core aur Desktop Experience options ki baat karte hain. Installation ke bare minimum aur practical RAM allocation ko ek na samjhein. Instructor ke classroom example mein 1–2 GB minimum-style values aur 4–8 GB ka practical starting range aata hai, lekin actual need installed roles aur workloads par depend karegi. Aapki host machine mein 8–16 GB RAM aur SSD ho to chhoti lab manageable ho sakti hai. Agar HDD slow ho, CPU constrained ho, ya multiple VMs chal rahi hon, to lag/latency ka impression aa sakta hai. Instructor apni tower machine aur purane refurbished laptop ke examples dete hain.

**Student (A:109–110):** Sir, pichli baar VMware use kiya to problem thi; is baar aapke installer se nahin aayi. Kya pehle mujhe use karna nahin aata tha?

**Instructor (A:111–128):** Nahin, aisa zaroori nahin. Version compatibility, operating system, hardware support aur updates farq daal sakte hain. Kabhi user jis product ko pasand karta hai uski chhoti problems bhi accept kar leta hai. Motorbike change karne ki misaal deta hoon: nayi bike aapki apni choice ho to uski learning curve bhi accept karte hain. Workstation ke purane 15/16 releases aur naye versions ki functionality alag ho sakti hai. Ab jab server mein login karta hoon, screen resize ho rahi hai; Ctrl+Alt se host par wapas aa sakte hain aur guest ke andar tools ka fayda saamne hai.
