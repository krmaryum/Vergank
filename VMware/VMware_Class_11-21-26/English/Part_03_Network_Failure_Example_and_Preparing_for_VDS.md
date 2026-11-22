# VMware November 21, 2026 — Part 03 — Network Failure Example and Preparing for VDS

**Coverage:** Source lines 179–277 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Classroom screen-sharing interruption

**Instructor/classroom discussion:** The instructor experiences a slow connection and a screen freeze while drawing. Students confirm when they can see three boxes. He explains that his core network had been working the night before but is behaving poorly during the session. The classroom waits while he continues the diagram.

## 2. Four-host topology illustration

**Instructor/classroom discussion:** He draws four ESXi hosts with virtual switches, then physical switches to which uplinks connect. The management/core and storage traffic are on separate networks. In the hypothetical setup, one host has a connection to an unexpected physical switch. He assigns an example VM IP and subnet mask to demonstrate how a network mismatch becomes obvious only after a host change.

## 3. Problem after HA restart or migration

**Instructor/classroom discussion:** A VM may be powered on on another host, but the virtual-to-physical connectivity path can be wrong. In that case users cannot reach the VM or its services. The instructor emphasizes that cluster availability is not only compute and storage availability: consistent networking matters, too.

## 4. Dedicated VM traffic network

**Instructor/classroom discussion:** The instructor proposes creating a separate virtual switch and network for VM workloads, instead of mixing VM traffic casually with the management or storage network. On each ESXi host he opens Configure, Virtual Switches and Add Networking. He presents the available wizard choices: VMkernel network adapter, virtual machine port group and physical network adapter.

## 5. VMkernel and port-group demonstration

**Instructor/classroom discussion:** He first selects the VMkernel option, adds a new switch and assigns available physical NICs in the example, identified as adapters 3 and 4. Adapters 0 and 1 are already used for the core network and another for storage. He then enters a network name, an IP such as 10.0.0.101, a mask and a gateway value. Next he creates a VM port group, naming it for the data-center or VM network.

## 6. Repeat on every ESXi host

**Instructor/classroom discussion:** He repeats the concept on Host 2 with another IP such as 10.0.0.102, and explains that the same port-group name can appear on different hosts. For Host 3 and Host 4 he applies the corresponding host-local configuration. His next objective is to manage the VM network consistently at the data-center level through vCenter.

## 7. Why the lesson is interview-relevant

**Instructor/classroom discussion:** The instructor says the network-virtualization lab may look complicated but is a very important area for VMware interviews. He repeatedly asks students to watch the procedure closely and practice it themselves, because observing the trainer click through the interface is not the same as building a working environment.
