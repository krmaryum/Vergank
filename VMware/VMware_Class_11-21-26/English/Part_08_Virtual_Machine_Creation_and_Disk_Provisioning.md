# VMware November 21, 2026 — Part 08 — Virtual Machine Creation and Disk Provisioning

**Coverage:** Source lines 566–625 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Launching the VM wizard

**Instructor/classroom discussion:** In vCenter the instructor begins the virtual-machine creation procedure and selects a suitable host, cluster or resource location, then specifies a VM name and other required selections. He relates each step back to the infrastructure already built: compute hosts, datastore and network assignment.

## 2. Compatibility, guest OS and hardware

**Instructor/classroom discussion:** The class discusses VM compatibility options, guest operating system selection and virtual hardware configuration. The instructor explains that the VM specification needs to correspond to the OS being installed and the resources allowed by the environment.

## 3. ISO, templates and repeated installations

**Instructor/classroom discussion:** The instructor asks whether an administrator should reinstall the same operating system repeatedly for every VM. He introduces the operational reason for using reusable installations, templates or cloning approaches, rather than treating every VM as an entirely new manual build.

## 4. Network adapter and hot-plug settings

**Instructor/classroom discussion:** While configuring the VM he refers to its network attachment and resources, then recalls the previous hot-plug lesson. The class discusses enabling supported hot-add/hot-plug facilities so that certain resource changes may be made with less disruption, depending on platform and guest support.

## 5. Thin versus thick provisioning

**Instructor/classroom discussion:** The instructor spends time distinguishing thin and thick virtual disks. A thin-provisioned disk can have a logical capacity larger than the space initially consumed, while thick provisioning reserves a defined disk allocation according to the selected format. He demonstrates how the storage or datastore choice affects available provisioning options.

## 6. Student asks about changing the disk format

**Instructor/classroom discussion:** The discussion turns to whether an existing thin disk can be converted to thick, and vice versa. The instructor explores options in Edit Settings and during migration. He explains that changing the storage location or storage format may expose a desired option not directly shown in the current view.

## 7. Compute migration versus storage migration

**Instructor/classroom discussion:** The instructor stresses that moving a VM between compute hosts is different from moving its virtual disks between datastores. Here the goal is storage conversion or relocation, so he selects storage migration rather than compute-only migration.
