# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 13 — BOOTMGR, NTLDR, hibernation, Winload aur BCD (Source B:235–243)

**Instructor (B:235–236):** **BOOTMGR** ko Windows boot loader/boot manager ke taur par introduce kiya gaya. Instructor batate hain ke purane Windows versions mein **NTLDR** use hota tha. Interviewer pooch sakta hai "Windows ka boot loader kya hai?" Woh repair/restore possibilities ko discuss karte hain aur kehte hain boot-related files bhi recover ki ja sakti hain.

**Instructor (B:237–239):** Boot Manager ko samjhane ke liye laptop ki **hibernation/suspend** misaal dete hain: aadmi laptop band karke ghar le gaya, kholne par kabhi jaldi login screen nazar aa jati hai. Instructor isey normal full cold boot se compare karte hain. Lecture mein **winresume.exe** ko hibernation resume path aur **winload.exe** ko normal startup path se relate kiya gaya hai.

**Instructor (B:240–242):** Normal boot mein winload.exe agla Windows loading stage handle karta hai. Agar OS/boot files corrupt ho jayein to **BCD — Boot Configuration Data**, Windows recovery tools aur "Repair your computer" option ki madad se troubleshooting/repair ki ja sakti hai. Instructor restore points ko bhi discuss karte hain aur kehte hain ke system ready karne ke baad recovery planning zaroor karein.

**Instructor (B:243):** Winload.exe se Windows kernel loading ki discussion shuru hoti hai. Instructor yaad dilate hain ke front-end par logo nazar aa raha hota hai lekin background mein boot ke kai steps complete ho chuke hote hain.

