# VMware November 21, 2026 — Part 04 — vSphere Distributed Switch Banana

**Coverage:** Source lines 278–374 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Standard switch versus distributed switch

**Instructor / classroom discussion:** vSphere Standard Switch har ESXi host par separately configure hota hai, jabke vSphere Distributed Switch (VDS) ko vCenter se data-center level par manage kiya jata hai. Instructor Networking inventory mein data center object par right-click karke Distributed Switches > New Distributed Switch select karte hain. Yeh class ka main practical hissa hai.

## 2. Switch name and compatibility version

**Instructor / classroom discussion:** Woh default naam DSwitch rakhte hain, lekin kehte hain ke company ya data-center name ke hisaab se switch ka naam rakhna bhi theek hai. Wizard distributed switch ka compatibility version poochta hai. Instructor 8.x, 9.0 aur 9.1 jaise hosts ka example dete hain. Agar purana ESXi host bhi add karna ho to uski compatibility check karni chahiye. Purana switch version choose karne se kuch naye features available nahi honge.

## 3. Student asks about newer ESXi versions

**Instructor / classroom discussion:** Student poochta hai ke agar switch version 7 choose karein to kya version 9 ke naye features bhi milenge? Instructor jawab dete hain ke nahi: compatibility ka lower version select karne par newer features automatically nahi milte. Switch version upgrade kiya ja sakta hai; baad mein older host ko add karne ke liye downgrade simple nahi hota.

## 4. Configuring uplink count

**Instructor / classroom discussion:** Ab wizard uplinks ki count poochta hai. Instructor samjhate hain ke uplink ESXi host ke physical network adapter se distributed switch ka connectivity path hai. Do paths hone se redundancy mil sakti hai agar configuration sahi ho. Woh four uplink slots rakhte hain, lekin filhal do use karne ka plan hai; baqi future ke liye khali reh sakte hain.

## 5. Finishing VDS creation

**Instructor / classroom discussion:** Instructor baqi advanced options ko is session mein skip karte hain aur Next > Finish kar dete hain. Ab naya distributed switch vCenter mein nazar aata hai. Woh samjhate hain ke sirf switch object ban jana poora kaam nahi. Ab distributed port groups aur ESXi host uplinks map karne hain.

## 6. Diagram of an end-to-end path

**Instructor / classroom discussion:** Woh diagram mein wapas chaar ESXi hosts aur common distributed switch ka concept dikhate hain. Management ke liye 192.168.0.x, storage ke liye 172.16.x aur VM traffic ke liye 10.0.0.x example network use karte hain. Yeh class ke sample subnets hain. Diagram ka maqsad traffic types separate rakhna aur redundant paths samjhana hai.
