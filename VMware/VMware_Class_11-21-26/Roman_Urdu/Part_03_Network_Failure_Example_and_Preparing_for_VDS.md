# VMware November 21, 2026 — Part 03 — Network Example aur VDS ki Tayyari

**Coverage:** Source lines 179–277 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Classroom screen-sharing interruption

**Instructor / classroom discussion:** Diagram banate hue instructor ka network slow hota hai aur screen freeze hoti hai. Students confirm karte hain ke unko teen boxes nazar aa rahe hain. Instructor batate hain ke raat ko core network theek tha, lekin class mein connection problem de raha hai. Phir woh diagram continue karte hain.

## 2. Four-host topology illustration

**Instructor / classroom discussion:** Instructor chaar ESXi hosts aur unke virtual switches ka diagram banate hain. Phir physical switches aur uplink cables connect karte hain. Management/core aur storage traffic separate networks hain. Example mein ek host ki cable ghalat physical switch se connected hai. Woh VM ki example IP aur subnet mask bata kar samjhate hain ke host change hone par network mismatch samne aata hai.

## 3. Problem after HA restart or migration

**Instructor / classroom discussion:** VM doosre host par power on ho sakti hai, lekin physical network tak uska raasta ghalat ho to users aur doosri services us se communicate nahi kar sakti. Instructor ka point yeh hai ke HA aur cluster availability ke liye sirf CPU, RAM aur storage nahi, consistent networking bhi zaroori hai.

## 4. Dedicated VM traffic network

**Instructor / classroom discussion:** Instructor suggest karte hain ke VM workloads ke liye alag dedicated network banaya jaye, na ke management ya storage network par saara VM traffic rakh diya jaye. Har ESXi host par Configure > Virtual Switches > Add Networking open karte hain. Wizard mein VMkernel network adapter, VM port group aur physical adapter ke options dikhte hain.

## 5. VMkernel and port-group demonstration

**Instructor / classroom discussion:** Woh pehle VMkernel option select karte hain aur naya switch create karte hain. Example mein free physical NICs 3 aur 4 use karte hain; NICs 0 aur 1 core network ke liye aur doosra adapter storage ke liye allocated hai. Phir ek network name, example IP 10.0.0.101, subnet mask aur gateway enter karte hain. Is ke baad isi traffic ke liye VM port group create karte hain.

## 6. Repeat on every ESXi host

**Instructor / classroom discussion:** Host 2 par isi procedure ko doosri IP, masalan 10.0.0.102, ke saath repeat karte hain. Instructor kehte hain ke alag ESXi hosts par same port-group name rakh sakte hain. Host 3 aur Host 4 par bhi host-local networking banate hain. Agla maqsad yeh hai ke vCenter se data-center level par VM network centralize ho.

## 7. Why the lesson is interview-relevant

**Instructor / classroom discussion:** Instructor students ko yaad dilate hain ke yeh networking lab dekhne mein mushkil lag sakti hai, lekin VMware interviews mein bohat important hai. Woh kehte hain ke sirf instructor ko screen par kaam karte dekhna kaafi nahi. Har student ko khud switch aur network configure karna chahiye.
