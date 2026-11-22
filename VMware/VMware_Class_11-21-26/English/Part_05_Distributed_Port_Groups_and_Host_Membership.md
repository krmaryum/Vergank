# VMware November 21, 2026 — Part 05 — Distributed Port Groups and Host Membership

**Coverage:** Source lines 375–475 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. One switch, multiple logical networks

**Instructor/classroom discussion:** The instructor draws three logical networks within the distributed-switch design: VMware Lab, Cloud Lab and Windows Lab. A switch is not itself the same thing as one subnet or one department. A single VDS can carry separate port groups and VLAN-backed networks. He asks which network a new VM should join; it depends on the VM role.

## 2. Two virtual NICs are possible

**Instructor/classroom discussion:** He explains that a virtual machine can have more than one virtual network card. For example, one virtual NIC could attach to the VMware Lab network while another attaches to Cloud Lab. He relates this to real organizations that separate Sales, IT, HR, Purchasing and Marketing, or use VLAN IDs such as 2, 3 and 5.

## 3. Creating the first distributed port group

**Instructor/classroom discussion:** He right-clicks the distributed switch and creates a port group, using VMware Lab as an example name. The wizard displays port binding, port allocation, number of ports, VLAN and policies. He favors Static Binding for the class and discusses Ephemeral as another available option. He also demonstrates Elastic port allocation and chooses a number of ports according to projected VM requirements.

## 4. VLAN assignment and network-team coordination

**Instructor/classroom discussion:** The wizard can associate a port group with a VLAN ID if the organization uses VLANs. The instructor says the network team normally supplies the VLAN details. In this isolated lab he can keep the VLAN setting as None. He leaves additional policy topics for other training and completes the port group.

## 5. Second port group

**Instructor/classroom discussion:** He creates another port group named Cloud Lab. This one can have a different port count from VMware Lab. The instructor emphasizes that the numbers do not have to match across groups; each logical network can be designed for its own requirements.

## 6. Host addition is not automatic

**Instructor/classroom discussion:** The new VDS and its distributed port groups do not yet mean that all ESXi hosts are participating. He opens Add and Manage Hosts, chooses Add Hosts and selects the hosts intended to use the switch. It is possible to add only two or three instead of all four, depending on the project.

## 7. Mapping physical NICs to uplinks

**Instructor/classroom discussion:** The instructor reviews which NICs are in use: 0 and 1 for core traffic, 2 for storage, and 3 and 4 intended for VM network traffic. In the host-addition wizard he selects the free/intended physical adapters and maps them to distributed switch uplinks. He checks host configuration to avoid choosing the wrong card.

## 8. VMkernel mapping and wizard finish

**Instructor/classroom discussion:** The wizard shows existing VMkernel interfaces, including an example vmk2. The instructor discusses assigning or selecting network placement, then moves through VM migration/port-group steps and finishes host addition. Afterward the UI shows network tasks and a temporary alarm related to a connectivity change. He checks whether all four hosts joined successfully.
