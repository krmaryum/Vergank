# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 1 — Windows booting process interview mein kyun important hai?

**Instructor (B:1–4):** Abhi humne Windows Server ki sirf installation ki hai, lekin installation ke baad bhi bohat se sawalat paida ho jate hain. Company mein server build kaise hota hai? Kaun se procedures follow hote hain? Kaunsa server OS aur kis hardware configuration ka selection karna chahiye? Ab ek bohat common interview question hai: Server ko power on karte waqt Windows ka booting process kya hota hai? Sirf ye batana k button dabaya, logo nazar aaya, please wait likha aaya aur login screen khul gayi—ye technical answer nahin hai. Experienced candidates se bhi fundamentals poochhe ja sakte hain.

**Instructor (B:5):** Hum Microsoft server administration curriculum padh rahe hain. Maqsad ye hai ke hum booting process ko professional interview mein technically explain kar sakein.

**Instructor (B:6–10):** Computer power on karte hi ek important stage **POST**, yani **Power-On Self-Test**, hoti hai. Power supply motherboard ke through CPU, RAM aur storage jaise components ko power deti hai. Hardware aur firmware initialization checks mein fault samne aa sakta hai. Model ke mutabiq beep codes, front-panel LEDs ya diagnostic messages milte hain. HPE ya Dell servers mein LEDs ka exact meaning vendor ki documentation se verify karna hota hai.

**Instructor (B:11–16):** Kal humne remote management port discuss kiya tha. HPE mein ise aam tor par **iLO** aur Dell PowerEdge mein **iDRAC** kehte hain. Doosre vendors ke apne management systems hote hain. Agar server boot nahin ho raha aur beep ya LED se problem samajh nahin aa rahi, to out-of-band management console check karein. Wahan hardware health aur error logs mil sakte hain. Vendor support available ho to screenshot ya logs le kar support case raise karein.

**Instructor (B:17–27):** Physical hardware ka support contract aur Windows OS ka license do alag cheezen hain. Companies hardware warranty aur support agreement purchase kar sakti hain. Contract ki conditions ke mutabiq manufacturer fault diagnose karta hai, replacement component deliver karta hai, aur kabhi engineer ko data center bhejta hai.

**Instructor (B:28–30):** Apne experience se example deta hoon. Ek server 2018 se rack mein laga hua tha, lekin us par ab tak OS install nahin hua tha. Server dekhne mein bilkul naya lagta tha. Jab maine deployment ke liye use power on kiya to hardware alarm aaya.

**Instructor (B:31–38):** Pehle laga ke RAM ka fault hai. Maine HPE support case raise kiya. Server mein taqreeban baarah RAM modules the, replacement memory deliver hui aur engineer ne replace ki, lekin error wahi raha. Aage diagnose karne par motherboard faulty nikla. Phir naya motherboard aaya, replace hua aur server sahi start ho gaya. Kyun ke us par koi critical workload nahin chal raha tha, is liye response P1 incident jaisi urgency wala nahin tha.

**Instructor (B:39–44):** Support contract na hota to motherboard replace karna kaafi mehnga pad sakta tha. Isi liye hardware support zaroori hai. POST aur alarms se OS start hone se pehle hardware problems identify ki ja sakti hain. Sab ko clear hai? Class ne kaha: clear hai. Ab agar initial checks pass ho jayein to agla stage kya hoga?

