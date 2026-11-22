# Day 03 Part A — Windows Defender Firewall, profiles, rules and student question

**Original-source reference:** A:195–231.

**Instructor (A:195–204):** Ab Windows Defender Firewall check karte hain. Run dialog mein `firewall.cpl` type karne se firewall console aa sakti hai. Network settings se bhi relevant control milta hai. Firewall profiles aur enabled/disabled states ko dekhiye. Instructor green security status ki baat karte hain aur batate hain ke default mein firewall on ho sakti hai; production policy change karne se pehle zaroorat aur impact samjhein.

**Instructor (A:205–213):** 'Turn Windows Defender Firewall on or off' jaise options aate hain, lekin sirf experiment ke liye firewall disable mat karein. 'Block all incoming connections, including those in the list of allowed apps' ka option allowed exceptions ko bhi block kar sakta hai; is se connectivity toot sakti hai. Advanced firewall console mein inbound aur outbound rules ko granular tareeqe se configure kiya jata hai.

**Instructor (A:214–226):** Classroom mein policy aur organization-wide configuration par baat hoti hai. Kisi company ke server par Windows firewall off dikhne ka matlab yeh ho sakta hai ke doosra network security architecture deploy hai, lekin isey automatically safe assume nahin karna. Client-server connectivity ke liye ports, service requirements aur policy ko consider karna hota hai.

**Student / Instructor (A:227–231):** Sarfraz ji firewall aur file server connectivity par sawal karte hain. Instructor unhein yaad dilate hain ke group policy se domain machines par rules manage kiye ja sakte hain. Student kehta hai, 'Haan, mera answer clear ho gaya.' Lecture mein yeh point aata hai ke firewall enable rakh kar bhi file-sharing services ke liye required rules allow kiye ja sakte hain.
