# Day 03 — Part B: Roman Urdu Classroom Discussion

## Section 12 — Legacy BIOS, UEFI aur storage boot sector ka introduction (Source B:221–234)

**Instructor (B:221–226):** Firmware decide karta hai ke system kis boot path ko use karega. Legacy BIOS ke muqablay mein **UEFI** modern architecture hai. Instructor ke mutabiq UEFI newer hardware aur operating systems ke liye suitable hota hai, boot behavior zyada modern hota hai, aur configuration features behtar milte hain.

**Instructor (B:227–230):** Agar naya HPE/Dell server liya ho aur old legacy mode choose kar diya ho to instructor use recommend nahin karte. Unka kehna hai ke new server deployments mein UEFI prefer karein. Ab firmware se boot device identify hota hai, chahe system mein do ya teen disks hon. Disk ke beginning structures aur Windows boot files tak agla stage pahunchta hai. Instructor MBR/GPT par baad mein aane ka keh kar pehle **Volume Boot Sector** samjhate hain.

**Instructor (B:231–232):** Woh book ke **index** ki misaal dete hain. Jaise book ke index se chapters ke page numbers milte hain, waise disk ke structures se system ko partitions aur boot files ki location tak pahunchne mein madad milti hai. Instructor C, D aur E drives ki misaal se disk layout samjhate hain.

**Instructor (B:233–234):** Pichhli Windows installation mein kuch hidden/system partitions aur C drive bani thin. Instructor lagbhag **100 MB** ke boot-related partition ka hawala dete hain, aur kehte hain ke yahin se required boot files milti hain. User ke saamne Windows ka logo blink karta hai, lekin backend mein boot ke multiple steps ho rahe hote hain. Agla topic Windows Boot Manager hai.

