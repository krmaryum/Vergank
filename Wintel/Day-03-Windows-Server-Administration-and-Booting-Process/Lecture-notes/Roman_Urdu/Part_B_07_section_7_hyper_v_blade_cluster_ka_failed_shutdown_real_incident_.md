# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 7 — Hyper-V blade cluster ka failed shutdown: real incident (Source B:136–153)

**Instructor (B:136–138):** Mere ek training batch ke student ki company mein **Microsoft Hyper-V cluster** chal raha tha, aur takreeban **12 blade servers** cluster ka hissa thay. Hum aage clustering aur Hyper-V role installation detail se padhenge. Filhaal yeh real-life incident samajhiye.

**Instructor (B:139–143):** Company ne data center ka ek specific section planned shutdown karna tha. Student ko rack mein maujood clustered hosts power off karne thay. Usne cluster coordination aur complete shutdown process samjhe baghair direct servers/OS shutdown kar diye. Use blade enclosure ke complete shutdown ka tareeqa bhi nahin pata tha.

**Instructor (B:144–148):** Data center mein kuch lights blink kar rahi thin, lekin usne unhein waisa hi chhor diya. Power/UPS wapas aane ke baad blades ki displays aur operating systems kisi tarah start nazar aa gaye. Lekin enclosure aur cluster ki expected shutdown/startup sequence follow nahin hui thi; cluster wapas initialize nahin ho paaya.

**Instructor (B:149–153):** Us person ka qareeban **aath saal ka experience** tha, lekin yeh situation pehli martaba aayi thi. Company ko external OS/cluster technical support leni padi aur paid case raise hua. Hardware failure hota to OEM support ka role alag hota. Yeh incident dikhata hai ke **OS shutdown, blade power state aur cluster-wide shutdown** ko ek cheez samajhna khatarnak ho sakta hai.

