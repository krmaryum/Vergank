# VMware November 21, 2026 — Part 09 — SAN Expand Karna, RDM aur Migration

**Coverage:** Source lines 626–665 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Resource limitation during the demonstration

**Instructor / classroom discussion:** Disk migration demo ke dauran lab mein storage capacity kam par jati hai. Instructor batate hain ke target datastore mein sufficient free space na ho to migration complete nahi hoti. Yeh class nested/virtual storage use kar rahi hai, koi bada dedicated physical SAN nahi.

## 2. Adding capacity to the storage server

**Instructor / classroom discussion:** Instructor Windows-based storage server wali VM khol kar additional virtual disks add karte hain. Example mein 200 GB ki disk aur taqreeban 2 TB ki do disks shamil hain. Phir storage VM ko power on karte hain. Woh future classes ke liye extra capacity rakhna chahte hain taake baar baar storage VM restart na karni pare.

## 3. Windows Disk Management and iSCSI

**Instructor / classroom discussion:** Windows mein Disk Management use karke nayi disks recognize aur initialize karte hain, demo ke mutabiq GPT select karte hain, aur required formatting/volume preparation hoti hai. Server Manager > File and Storage Services > iSCSI ke andar storage publish karte hain taake existing iSCSI targets ke through VMware hosts tak pahunch sake.

## 4. Creating new virtual disks and naming them

**Instructor / classroom discussion:** Instructor Raw Disk, Gold SAN 01 aur Gold SAN 02 jaise names se storage objects banate hain. Size, dynamic/fixed allocation aur existing iSCSI targets ke options choose karte hain. Objects banane ke baad vCenter mein wapas aa kar storage rescan aur provisioning continue karte hain.

## 5. Shared SAN contention example

**Instructor / classroom discussion:** Shared SAN ko samjhane ke liye instructor do customers ka example dete hain. Ek normal workload use karta hai, doosra heavy workload chalata hai jis se utilization spikes aa sakte hain. Woh railway line ke paas ghar ka example dete hain: train ka shor aur vibration pareshan kare to tenant location change mangta hai. Isi tarah customer dedicated storage mang sakta hai.

## 6. Raw Device Mapping discussion

**Instructor / classroom discussion:** Lecture mein RDM yani Raw Device Mapping ka concept aata hai. Supported vSphere configuration mein suitable storage LUN ya device ko VM se map kiya ja sakta hai. Instructor VM Edit Settings mein Add RDM Disk option dikhate hain. Woh isay interview question samajhte hain aur batate hain ke RDM ordinary thin/thick VMDK jaisi cheez nahi.

## 7. Creating datastores from available SAN LUNs

**Instructor / classroom discussion:** Ab instructor available SAN LUNs se naye datastores create karte hain aur unko Gold SAN jaise names dete hain. Host select karke visible disk choose karte hain, datastore wizard complete karte hain aur formatting/discovery ka intezar karte hain. Nested lab ki wajah se process slow hai.

## 8. Trying the storage migration again

**Instructor / classroom discussion:** Additional datastore capacity nazar aane ke baad instructor storage-only migration dobara try karte hain. Wizard mein destination aur thin/thick format ke options review karte hain. Woh samjhate hain ke suitable migration ke dauran disk format change ho sakta hai agar space aur compatibility available hon. Storage slow hone ki wajah se kuch intezar hota hai.
