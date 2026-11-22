# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 16 — Modern Windows versions, UEFI boot mode, Rufus aur MBR/GPT (Source B:259–270)

**Instructor (B:259–261):** Desktop load ho gaya to basic Windows startup complete ho gaya. Instructor batate hain ke Windows Vista, 7, 8, 10, 11 aur Windows Server 2012 se 2025 tak boot process ke core ideas similar hain, is liye interview mein modern Windows ka systematic answer dena chahiye; purane unsupported systems ki unnecessary detail mein na jayein. Ye unka classroom generalization hai; exact Windows versions ke boot components alag ho sakte hain.

**Student (B:262):** Sir, to phir hum BIOS ke bajaye UEFI ki explanation dein?

**Instructor (B:262–263):** Haan, agar machine UEFI mode mein configured aur install hui hai to usi mode ka boot path explain karein. Agar aap OS ko UEFI mode mein install karein aur baad mein bina migration/reconfiguration ke legacy mode mein switch kar dein to system boot nahin bhi ho sakta. OS installation aur firmware mode ka match bohat important hai.

**Instructor (B:263–265):** Kal bootable USB banate waqt humne **Rufus** use kiya tha. Universal USB Installer bhi milta hai, jo instructor ke mutabiq Linux media ke liye useful ho sakta hai. Rufus mein bootable USB banate waqt partition scheme aur target boot mode select karne ke options hote hain. Agar hardware UEFI support karta hai aur aap UEFI deployment kar rahe hain, to media ko bhi uske mutabiq prepare karein.

**Instructor (B:265–267):** Naye systems par firmware mein legacy/CSM aur UEFI boot choices ho sakti hain, model par depend karta hai. Agar configuration reset ho jaye, CMOS/RTC issue ke baad boot priority ya mode badal jaye, to installed OS load nahin hoga. Is liye troubleshooting ke waqt check karein ke disk kis mode mein install hui thi aur current firmware usi mode mein boot kar raha hai.

**Instructor (B:267–269):** Lecture ki slides OneDrive par share kar di hain. Instructor kehte hain ke boot process mein ek topic jaan boojh kar skip kiya hai: **MBR (Master Boot Record)** aur **GPT (GUID Partition Table)**. Ye disk-partitioning styles hain; in par agle hafte detail mein baat karenge, kyun ke aaj waqt kam hai.

**Instructor (B:270):** Aaj zyada hands-on labs nahin hui. Pichhli class mein OS installation hui thi aur aaj VMware Tools discuss/install kiye thay; baqi session theoretical raha. Instructor students ko advise karte hain ke weekend se pehle recording dobara sun kar concepts revise karein.

