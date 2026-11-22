# VMware November 21, 2026 — Part 05 — Distributed Port Groups aur Hosts Add Karna

**Coverage:** Source lines 375–475 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. One switch, multiple logical networks

**Instructor / classroom discussion:** Instructor ek distributed switch ke andar teen logical networks banate hain: VMware Lab, Cloud Lab aur Windows Lab. Woh batate hain ke ek switch ka matlab sirf ek network nahi hota. Ek VDS par multiple port groups aur VLAN-based networks ho sakte hain. Nayi VM ko kis network se connect karna hai, yeh VM ke role par depend karega.

## 2. Two virtual NICs are possible

**Instructor / classroom discussion:** Instructor kehte hain ke ek VM mein do ya zyada virtual NICs lag sakti hain. Ek NIC VMware Lab se connected ho aur doosri Cloud Lab se, to VM multiple networks par kaam kar sakti hai. Real companies mein Sales, IT, HR, Purchasing aur Marketing ke separate VLANs ho sakte hain, masalan VLAN IDs 2, 3 aur 5.

## 3. Creating the first distributed port group

**Instructor / classroom discussion:** Woh distributed switch par right-click kar ke naya port group banate hain aur naam VMware Lab dete hain. Wizard mein port binding, allocation, ports ki tadaad, VLAN aur policies ke options aate hain. Instructor class ke liye Static Binding choose karte hain, Ephemeral option ka zikr karte hain, aur Elastic port allocation explain karte hain. Ports ki count VM requirements ke mutabiq select hoti hai.

## 4. VLAN assignment and network-team coordination

**Instructor / classroom discussion:** Agar company VLAN use karti ho, to port group par VLAN ID assign ki ja sakti hai. Instructor kehte hain ke VLAN details aam tor par network team provide karti hai. Is lab mein VLAN use na karne par None choose karte hain. Baqi advanced policies ko future training ke liye chhor dete hain aur port group finish kar dete hain.

## 5. Second port group

**Instructor / classroom discussion:** Instructor doosra port group Cloud Lab ke naam se banate hain. Is mein ports ki count VMware Lab se kam ya zyada ho sakti hai. Woh samjhate hain ke har group ke liye same number of ports hona zaroori nahi; design workload ki requirement ke mutabiq hota hai.

## 6. Host addition is not automatic

**Instructor / classroom discussion:** VDS aur distributed port groups create karne ke baad bhi ESXi hosts automatically member nahi bante. Instructor Add and Manage Hosts > Add Hosts choose karte hain aur selected hosts ko VDS se associate karte hain. Project requirement ke mutabiq do, teen ya chaar hosts add kiye ja sakte hain.

## 7. Mapping physical NICs to uplinks

**Instructor / classroom discussion:** Instructor physical NIC allocation dobara check karte hain: 0 aur 1 core network, 2 storage, aur 3 aur 4 VM traffic ke liye. Add Hosts wizard mein in adapters ko distributed switch ke uplinks se map karte hain. Woh host configuration verify karte hain taake ghalat physical NIC select na ho.

## 8. VMkernel mapping and wizard finish

**Instructor / classroom discussion:** Wizard existing VMkernel interfaces, jaise vmk2, dikhata hai. Instructor interface ko identify karke network assignment ke options samjhate hain. Woh next steps se guzarte hain aur host addition finish karte hain. Baad mein kuch temporary connectivity alarms nazar aate hain. Woh check karte hain ke chaaron hosts successfully VDS mein add ho gaye hon.
