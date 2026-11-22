# VMware November 21, 2026 — Part 08 — Virtual Machine aur Disk Provisioning

**Coverage:** Source lines 566–625 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Launching the VM wizard

**Instructor / classroom discussion:** vCenter mein instructor VM creation wizard open karte hain aur suitable host, cluster ya resource location choose karte hain. VM name aur baqi required selections enter karte hain. Har step ko woh pehle banaye hue infrastructure ke saath relate karte hain: compute hosts, datastore aur network.

## 2. Compatibility, guest OS and hardware

**Instructor / classroom discussion:** Class mein VM compatibility, guest operating system selection aur virtual hardware settings discuss hoti hain. Instructor samjhate hain ke VM ki configuration us OS aur workload ke mutabiq honi chahiye jo install aur run karna hai, aur environment ki available capacity ke andar rehni chahiye.

## 3. ISO, templates and repeated installations

**Instructor / classroom discussion:** Instructor sawal karte hain: agar company ko bohat si VMs chahiye hon to kya har baar operating system manually install karenge? Is se templates, cloning aur reusable standardized builds ki zaroorat samajh aati hai. Har VM ko zero se manually banana productive approach nahi hoti.

## 4. Network adapter and hot-plug settings

**Instructor / classroom discussion:** VM configure karte hue woh network attachment aur resources review karte hain aur pichhli class ka hot-plug topic yaad dilate hain. Supported hot-add settings enable hone se kuch resources ko kam interruption ke saath change kiya ja sakta hai, lekin support hypervisor aur guest OS par depend karta hai.

## 5. Thin versus thick provisioning

**Instructor / classroom discussion:** Instructor thin aur thick disks ka farq detail mein samjhate hain. Thin disk ki logical capacity badi ho sakti hai, lekin shuru mein actual consumed storage kam hoti hai. Thick disk mein selected format ke mutabiq disk space reserve hoti hai. Wizard mein datastore aur storage choice ke mutabiq available provisioning options change ho sakte hain.

## 6. Student asks about changing the disk format

**Instructor / classroom discussion:** Class mein sawal aata hai ke existing thin disk ko thick, ya thick ko thin kaise kiya jaye. Instructor Edit Settings aur migration wizard mein options check karte hain. Woh batate hain ke storage change ya migration ke waqt woh format option mil sakta hai jo current screen mein nahi mil raha.

## 7. Compute migration versus storage migration

**Instructor / classroom discussion:** Instructor clear karte hain ke VM ko ek ESXi host se doosre host par move karna aur uski virtual disks ko ek datastore se doosre datastore par move karna alag operations hain. Is example mein goal disk format ya location change karna hai, is liye storage migration select hoti hai.
