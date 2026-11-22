# VMware November 21, 2026 — Part 06 — Connecting VMs to VDS and Practice Advice

**Coverage:** Source lines 476–520 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Move an existing VM to a distributed port group

**Instructor/classroom discussion:** He selects a VM on Host 2 whose network adapter still points to the host-local VM Network. He edits VM settings, browses available networks and chooses a distributed port group such as VMware Lab or Cloud Lab. After confirming, the VM network backing is changed from the previous port group to the selected distributed port group.

## 2. Why consistent VDS backing helps migration

**Instructor/classroom discussion:** He points out that a distributed port group can be available on all participating hosts. Therefore a VM migrating or restarting on another host can maintain equivalent network placement, provided the underlying uplinks, VLANs and connectivity are correctly configured. He contrasts this with the risk of inconsistent host-local standard switches.

## 3. Inspect rather than alter production environments

**Instructor/classroom discussion:** Students are encouraged to open the Networking section in their own environments, identify the distributed switch icon and review configuration tabs and port groups. The instructor distinguishes observation from making changes: the goal is first to understand how a real deployed environment has been built.

## 4. Hands-on priorities and exam emphasis

**Instructor/classroom discussion:** He especially recommends practicing the SAN storage lab and the VDS lab with your own hands. One student performing the lab while others watch is not enough. The instructor says these topics are important for interviews and examination scenarios because they require understanding physical-to-virtual connectivity and storage concepts.

## 5. Break, vCenter domain question and connection issues

**Instructor/classroom discussion:** He announces a short break before the VM chapter. A student asks about joining vCenter to the AD domain. The instructor says this will be done at the end because restarting vCenter can take time and he does not want to interrupt the lesson. He also mentions instability with his internet provider and a previous ISP issue involving an unexpectedly changed public IP.
