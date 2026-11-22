# VMware November 21, 2026 — Part 04 — Creating the vSphere Distributed Switch

**Coverage:** Source lines 278–374 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Standard switch versus distributed switch

**Instructor/classroom discussion:** A vSphere Standard Switch is configured per ESXi host, whereas the vSphere Distributed Switch (VDS) is managed through vCenter at the data-center level. The instructor opens the Networking inventory, right-clicks the data-center object, and selects Distributed Switches > New Distributed Switch. This is the main practical demonstration of the class.

## 2. Switch name and compatibility version

**Instructor/classroom discussion:** He keeps a default switch name such as DSwitch, while noting that an organization can use a name containing its data-center or project name. The wizard asks for the distributed switch compatibility version. He discusses hosts at versions such as 8.x, 9.0 and 9.1, and the importance of supporting the oldest ESXi host intended to join. He explains that choosing an older switch version can reduce newer capabilities.

## 3. Student asks about newer ESXi versions

**Instructor/classroom discussion:** A student asks whether selecting an older version, such as 7, will allow all newer version-9 features as well. The instructor replies that old compatibility does not make the newer feature set appear: it restricts the features to those supported by the selected switch version. He adds that a switch can be upgraded, while downgrading to accommodate older hosts may be problematic.

## 4. Configuring uplink count

**Instructor/classroom discussion:** Next the wizard asks how many uplinks to provision. The instructor shows that one uplink represents a path from the distributed switch to a host physical network interface. More than one path can offer redundancy if configured properly. He leaves a default of four uplink slots even though only two may be used immediately. Remaining slots can be reserved for future changes.

## 5. Finishing VDS creation

**Instructor/classroom discussion:** He skips the other advanced settings for this class and clicks Next and Finish. The new distributed switch appears in vCenter. He explains that creating the switch object is only one step: the next tasks are to create distributed networks/port groups and then add ESXi hosts with their physical adapters.

## 6. Diagram of an end-to-end path

**Instructor/classroom discussion:** He returns to the drawing, showing four ESXi hosts connected to a common distributed switch concept. Management IPs are in a 192.168.0.x network, storage is on a 172.16.x network and the proposed VM network is on 10.0.0.x. The exact subnets in the class are demonstration values. The diagram is intended to separate traffic types and show redundant connectivity.
