# VMware November 21, 2026 — Part 07 — Why Virtual Machine Creation Comes After Infrastructure

**Coverage:** Source lines 521–565 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Instructor’s preferred learning sequence

**Instructor/classroom discussion:** He says some courses teach VM creation in the second or third lesson, but from production experience he prefers to establish the supporting infrastructure first. A VM requires CPU, RAM, storage and network. ESXi and clusters contribute compute; proper VM networks protect connectivity; storage design addresses availability and placement.

## 2. Storage redundancy caution within the lecture

**Instructor/classroom discussion:** He notes that their current lab vSAN setup does not yet have all desired redundancy, and similarly storage resilience depends on the SAN design. Their practical setup demonstrates concepts, not a complete production-grade fault-tolerant environment. He says the storage team normally takes responsibility for specialized storage work.

## 3. Service request and change management

**Instructor/classroom discussion:** A new VM is commonly requested through a ticketing or change process. The instructor relates this to earlier class discussions about ticketing tools and email requests. A change can involve implementation, configuration or troubleshooting and may need several teams to coordinate, unlike a straightforward incident handled by one responder.

## 4. Planning and approvals before provisioning

**Instructor/classroom discussion:** The instructor describes production workflows around submitting a request, validating what service will run, deciding resources and storage, and obtaining applicable approvals. He emphasizes that a VMware administrator should not treat VM creation as an isolated click-through exercise: capacity, security and operational coordination matter.
