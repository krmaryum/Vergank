# VMware November 21, 2026 — Part 09 — SAN Expansion, RDM and Disk Migration

**Coverage:** Source lines 626–665 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Resource limitation during the demonstration

**Instructor/classroom discussion:** While exploring disk migration, the instructor hits limited storage capacity in the lab. He explains that not every migration can complete if the target datastore lacks sufficient resources, and that the class is using virtual or nested storage rather than a large dedicated physical array.

## 2. Adding capacity to the storage server

**Instructor/classroom discussion:** He opens the VM that hosts the Windows-based storage service, adds more virtual disks, including an example 200 GB disk and two approximately 2 TB disks, then powers the storage VM back on. He mentions that storage VM reboots can interrupt a lab, so he allocates some extra space for later sessions.

## 3. Windows Disk Management and iSCSI

**Instructor/classroom discussion:** Inside Windows they use Disk Management to recognize and initialize the newly attached disks, choose GPT where demonstrated, and format or prepare volumes as needed. In Server Manager, File and Storage Services and the iSCSI area are used to expose storage to VMware hosts through the existing targets.

## 4. Creating new virtual disks and naming them

**Instructor/classroom discussion:** The instructor creates storage objects with names such as Raw Disk, Gold SAN 01 and Gold SAN 02. He walks through size selection, dynamic/fixed allocation options and using the available iSCSI targets. After creating the storage objects he returns to vCenter for a storage rescan and provisioning.

## 5. Shared SAN contention example

**Instructor/classroom discussion:** To explain shared storage performance, he imagines two customers sharing an environment. One user performs ordinary work; another runs resource-heavy jobs, causing utilization spikes that could affect neighbors. He compares this with living near a railway line: the traffic creates disturbance, so a customer may request a quieter, isolated location.

## 6. Raw Device Mapping discussion

**Instructor/classroom discussion:** The lecture introduces RDM, Raw Device Mapping, as a way to attach an appropriate storage LUN or device directly to a VM in supported vSphere configurations. The instructor opens VM Edit Settings and looks for Add RDM Disk. He treats RDM as an interview topic and distinguishes it from an ordinary thin/thick VMDK.

## 7. Creating datastores from available SAN LUNs

**Instructor/classroom discussion:** He proceeds to create datastores from the newly offered storage, with names related to Gold SAN. He selects a host, chooses the disk/LUN visible to that host, runs the datastore creation wizard and waits for formatting or discovery to complete. Performance is slow in the nested lab.

## 8. Trying the storage migration again

**Instructor/classroom discussion:** After additional datastore capacity appears, he retries a storage-only migration and looks at thin/thick destination format choices. The instructor says that the format can be adjusted during an appropriate migration, subject to available capacity. The lab pauses while migration works through the slow virtual storage.
