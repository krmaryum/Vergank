# VMware November 21, 2026 — Part 07 — Infrastructure ke Baad VM Creation Kyun

**Coverage:** Source lines 521–565 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Instructor’s preferred learning sequence

**Instructor / classroom discussion:** Instructor kehte hain ke kuch courses mein doosri ya teesri class mein VM banana sikha dete hain. Lekin production experience ke hisaab se unki preference yeh hai ke pehle infrastructure banaya jaye. VM ko CPU, RAM, storage aur network chahiye. ESXi aur cluster compute provide karte hain, VDS network consistency deta hai aur storage design availability ko support karta hai.

## 2. Storage redundancy caution within the lecture

**Instructor / classroom discussion:** Woh khud batate hain ke current lab ka vSAN setup abhi required redundancy nahi rakhta aur SAN resilience bhi storage design par depend karti hai. Yani class ki lab concept demonstrate karti hai, complete production-grade fault-tolerant architecture nahi. Storage ke specialized tasks aam tor par storage team karti hai.

## 3. Service request and change management

**Instructor / classroom discussion:** Company mein nayi VM ki request aam tor par ticketing ya change process se aati hai. Instructor earlier class mein ticketing tools aur email requests ka zikr yaad dilate hain. Change implementation, configuration ya troubleshooting ka kaam ho sakta hai aur aksar multiple teams coordinate karti hain. Simple incident kabhi ek responder handle kar sakta hai.

## 4. Planning and approvals before provisioning

**Instructor / classroom discussion:** Instructor production process explain karte hain: pehle request aati hai, phir service ka purpose samjha jata hai, resources aur storage choose hoti hai aur relevant approvals li jati hain. VMware administrator ke liye sirf VM wizard par Next click karna kaafi nahi; capacity, security aur operations coordination bhi zaroori hai.
