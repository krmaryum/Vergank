# VMware November 21, 2026 — Part 02 — Virtual Machine Requirements and Host Networking

**Coverage:** Source lines 119–178 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. VM ke basic resources

**Instructor/classroom discussion:** A virtual machine needs CPU, memory, network connectivity and storage. The instructor asks the students to name the resources, and they offer CPU, RAM, networking, a physical host, an ISO image and a hard drive. He accepts the ISO as useful for OS installation while emphasizing four primary resource categories: compute, memory, network and storage.

## 2. vCPU, memory and storage ownership

**Instructor/classroom discussion:** In the VMware interface, the instructor refers to vCPU, virtual memory and virtual networking. He says that the ESXi host supplies CPU and memory and supports the networking functions. Storage might be local, NFS, SAN or VMware vSAN, so the storage source must be identified in the environment. He distinguishes the infrastructure responsibilities rather than assuming all VM resources come from one location.

## 3. Cluster capacity

**Instructor/classroom discussion:** He shows four ESXi hosts in his vCenter cluster, each with approximately 32 GB RAM, giving around 128 GB total. The screen shows approximately 61 GB free. He discusses available processor capacity and asks students to distinguish processor counts from core counts. Some physical or nested host memory is already consumed by the hosts and infrastructure.

## 4. Inventory view and virtual switches

**Instructor/classroom discussion:** In vCenter inventory, he moves between Hosts and Clusters, VMs, Storage and Networking. Under an ESXi host he opens Configure and Virtual Switches. Each host currently has separate virtual switches for the core/management network and storage connectivity. The guest VM shown is currently connected to a VM Network port group on its host.

## 5. Why host-level network consistency matters

**Instructor/classroom discussion:** He asks: if VM01 runs on ESXi Host 2 and that host fails, what happens when the VM restarts or moves to Host 3? If the destination host has different port groups, VLANs, subnets or physical uplink placement, the VM may lose network connectivity even though the VM itself can run. The instructor promises a diagram to illustrate the failure scenario.
