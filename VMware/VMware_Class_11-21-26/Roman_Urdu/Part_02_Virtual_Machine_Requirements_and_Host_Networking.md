# VMware November 21, 2026 — Part 02 — VM Requirements aur ESXi Networking

**Coverage:** Source lines 119–178 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. VM ke basic resources

**Instructor / classroom discussion:** Virtual machine chalane ke liye CPU, RAM, network connectivity aur storage chahiye. Instructor students se poochte hain ke VM banane ke liye kya resources darkar hain. Students CPU, memory, network, physical host, ISO aur hard drive batate hain. Instructor kehte hain ke ISO operating system install karne ke kaam aati hai, lekin chaar main resources compute, memory, network aur storage hain.

## 2. vCPU, memory and storage ownership

**Instructor / classroom discussion:** VMware interface mein instructor vCPU, virtual memory aur virtual networking ki baat karte hain. Unke mutabiq ESXi host VM ko CPU aur RAM provide karta hai aur network functions bhi handle karta hai. Storage local datastore, NFS, SAN ya vSAN se aa sakti hai. Is liye sirf VM create karna kaafi nahi; administrator ko pata hona chahiye ke storage asal mein kahan se aa rahi hai.

## 3. Cluster capacity

**Instructor / classroom discussion:** Instructor vCenter mein chaar ESXi hosts dikhate hain. Har host mein taqreeban 32 GB RAM hai, yani total 128 GB ke qareeb. Screen par lagbhag 61 GB free dikh rahi hai. Woh processor count aur core count ka farq bhi poochte hain. Infrastructure khud bhi memory use karti hai, is liye saari installed RAM VM workloads ke liye free nahi hoti.

## 4. Inventory view and virtual switches

**Instructor / classroom discussion:** vCenter inventory mein Hosts and Clusters, VMs, Storage aur Networking sections samjhaye jaate hain. ESXi host select karke Configure > Virtual Switches khola jata hai. Har host par abhi core ya management network aur storage connectivity ke liye alag virtual switches hain. Example VM apne host ke VM Network port group se connected hai.

## 5. Why host-level network consistency matters

**Instructor / classroom discussion:** Instructor poochte hain: agar VM01 ESXi Host 2 par hai aur woh host fail ho jaye, to Host 3 par VM chalne ke bawajood network kyun fail ho sakta hai? Agar doosre host ke port groups, VLANs, subnets ya physical uplink connections match na karte hon, to VM ki network connectivity toot sakti hai. Is concept ko samjhane ke liye woh diagram banate hain.
