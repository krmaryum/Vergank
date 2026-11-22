# VMware November 21, 2026 — Part 10 — Active Directory Integration and Class Wrap-up

**Coverage:** Source lines 666–682 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Why the AD integration demo was postponed

**Instructor/classroom discussion:** A student had requested a domain-join demonstration earlier. The instructor returns to it near the end of the session to avoid spending class time waiting for a vCenter restart. He refers to instructions or images previously shared with the group.

## 2. Identity-source settings in vCenter

**Instructor/classroom discussion:** In vCenter Administration he goes to identity-related configuration and adds an Active Directory-based identity source. The wizard asks for information such as domain name, distinguished name, alias, account credentials and an LDAP server/DC location. The lab domain is described in the source with a VCPLAB-style name; students are told to follow the displayed syntax.

## 3. Credentials and controller selection

**Instructor/classroom discussion:** He discusses using a domain account with appropriate permissions, optionally a dedicated user provisioned by the AD team, and choosing a specific domain controller or the default behavior. The source includes spoken password-like text; that must be treated as exposed demo material, not as a password to reuse in a real lab or repository.

## 4. Completing and shutting down the lab

**Instructor/classroom discussion:** He saves the identity-source information and discusses making it the default where appropriate. At the end he navigates through vCenter and ESXi interfaces to shut down or power off lab VMs and hosts. He reviews the two principal topics covered today: configuring a vSphere Distributed Switch and beginning VM creation.

## 5. Open items and final question

**Instructor/classroom discussion:** He reminds students that the virtual machine chapter is not yet complete and more options will be covered in the next session. He invites questions. He also refers to Khalid’s pending home-lab hardware configuration question, saying he intends to examine the system specifications. The recording ends at that point rather than providing the full hardware recommendation.
