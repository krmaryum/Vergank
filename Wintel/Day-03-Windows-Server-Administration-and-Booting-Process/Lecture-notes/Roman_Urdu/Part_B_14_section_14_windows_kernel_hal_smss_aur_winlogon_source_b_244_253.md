# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 14 — Windows kernel, HAL, SMSS aur Winlogon (Source B:244–253)

**Instructor (B:244–247):** Instructor **HAL.dll** ko hardware abstraction aur drivers se linked stage ke taur par explain karte hain. Woh graphics card, network adapter, USB aur doosre device drivers ki misaal dete hain. Lecture mein kernel initialization ke "phase zero" aur "phase one" stages mention hote hain. Hardware faulty ho to OS boot bhi ho sakta hai magar specific device (jaise LAN adapter) kaam na kare.

**Instructor (B:248–250):** Agla naam hai **smss.exe**, Session Manager Subsystem. Instructor ke slide par aage kernel/system processes aur **winlogon.exe** likha hua hai. Unka explanation hai ke operating system apni system files aur environment initialize karta hai, aur graphical/login stage ki taraf badhta hai.

**Instructor (B:250–252):** Woh **16-bit aur 32-bit colors** ka example de kar graphical display ka fark samjhane ki koshish karte hain. Rainbow mein kitne colors hote hain, students se poochte hain; phir batate hain ke graphical representation ke different modes hotay hain. Yeh example original lecture ka hissa hai, lekin modern Windows graphics pipeline ka exact description technical notes mein alag hai.

**Instructor (B:252–253):** **Winlogon.exe** se user ke saamne sign-in interface aata hai. Username aur password enter karne ke baad authentication process hota hai. Ab instructor live Windows system mein accounts-related storage dikhate hain.

