# VMware Training Class — Detailed English Transcript

## Part 01: Classroom Discussion, Lab Readiness, Datastore Troubleshooting, and Introduction to Virtual Machines

**Lecture date:** November 21, 2026  
**Source coverage:** Original transcript lines 1–118 (of 682).  
**Method:** This is a detailed, dialogue-based English rendering rather than a topic summary. The original sequence, questions, answers, instructor examples, and conversational details are retained. Speaker numbers reflect the source, not verified identities. Unclear audio is marked rather than guessed. Technical assertions are presented as the instructor said them, not independently verified.

### 1. Greetings and Technical Setup (Source lines 1–28)

**Speaker 1:** Good morning, everyone.

**Speaker 2:** [Several remarks in the original automatic transcript are unclear. The speaker seems to be opening or navigating something and mentions a database, software, and a scrolling menu. The words are not sufficiently reliable to reconstruct accurately.]

**Speaker 2:** [The source then includes an informal exchange partly in Urdu; portions are unclear.] Is the screen visible to everyone?

**Speaker 1:** Yes, sir.

**Speaker 2:** Perfect.

**Speaker 1 (Instructor):** Actually, I shared my screen a little late because my server was powering on. It has powered on now. Let me log in to it once. Okay, okay.

### 2. Review of the Previous Class and Lab Practice (Source lines 29–44)

**Speaker 1 (Instructor):** In the previous class, we saw how to configure HA on a cluster in vCenter, how to configure DRS, how to configure vMotion, and how to create affinity rules and similar settings. Right? Before we start today's session, how is your practice going?

**Speaker 3:** Sir, I haven't been able to practice at all.

**Speaker 1 (Instructor):** And Khalid, I'm sorry. Maybe, to some extent, I am also responsible for your not being able to practice. You contacted me many times with questions. Today in class, we will discuss the server details you sent to me.

**Speaker 3:** Thank you very much.

**Speaker 1 (Instructor):** Certainly. I really wasn't getting even the minimum amount of time to respond, which is probably why I couldn't reply to your questions. Anyway, today we will check what minimum configuration you need so that you can do the lab. Right?

**Speaker 3:** Thank you very much.

**Speaker 1 (Instructor):** What about the rest of the members? Are you practicing?

**Another participant:** Yes, I am doing the lab and practicing the sessions.

**Goutham (Guest):** Sir, I have one question. When we allocate disks, for example 500 GB or 4 TB, for a VM or host, I noticed that only about 200 GB of free space was available in the KR lab. When I tried it there, it seemed to work. How is that possible?

**Speaker 1 (Instructor):** Yes, yes, you can do that comfortably. When we perform these labs, we can complete the whole lab within roughly 150 GB. The 4,000 GB, or 4 TB, being displayed or assigned is only virtual in this example. We are not actually using that entire amount. So we can do it.

**Participant:** Okay, okay. Sure, sir.

### 3. Why a Datastore May Not Appear After Adding an ESXi Host (Source lines 45–72)

**Participant:** Sir, I had another doubt. When we add a host to vCenter, I couldn't see the storage in the datastore view for that ESXi host. Then I attached an additional hard disk to the host, and only after that did the storage appear. Why might this happen?

**Speaker 1 (Instructor):** Okay. That is a VMware Workstation issue. Sometimes, when we have made an ESXi host a member of vCenter, this happens. Let me go to the vCenter Server console and cross-check. I select the cluster, and then I look at Datastores. Here, I can see the datastore information for all four ESXi hosts.

**Speaker 1 (Instructor):** But sometimes it does not show this. When that happens, you might think you made a mistake. According to my experience, no, it isn't necessarily your mistake. It can happen because we are using VMware Workstation for virtualization.

**Speaker 1 (Instructor):** In that case, I see two approaches: reinstall the ESXi host or reset the ESXi host. By reset, I mean opening its DCUI, the direct console interface, and checking the options there. Let me show you in VMware Workstation.

**Speaker 1 (Instructor):** Open the ESXi host that is not showing the datastore. This can happen on some hosts, not necessarily all hosts. On the host's screen, you'll see 'Press F2 for DCUI.' Press F2 and log in.

**Speaker 1 (Instructor):** Near the bottom is an option called 'Reset System Configuration.' If you choose it and confirm with F11, the host's configuration is removed. You must configure that ESXi host again from the beginning. Any other settings you applied are also reset.

**Speaker 1 (Instructor):** It is similar to performing a hard reset on a mobile phone. When a phone is hard-reset, old data or settings may be removed; the phone sometimes asks whether you want to preserve data. For this ESXi reset, think of it as returning the host's configuration to the state of a clean installation. Afterward, assign an IP address to the host again and configure it. The disk should then become visible, according to this proposed lab procedure.

**Participant:** Okay, I see. So you are saying that it is a VMware Workstation issue rather than something we did wrong?

**Speaker 1 (Instructor):** Yes. I have seen this behavior in VMware Workstation. I have also submitted feedback. I haven't seen an update addressing it yet. I encountered it with the Workstation 17 family; I did not encounter the same issue with Workstation 16. If we open Help and About, the current version number may be in the 25/26 family, but I trace the behavior back to version 17.

**Speaker 1 (Instructor):** When you added another disk, the additional disk became visible, but the original expected drive still did not appear, correct?

**Participant:** Yes, the additional one appeared.

**Speaker 1 (Instructor):** Right. That is what I am describing.

> **Editorial caution, not part of the classroom dialogue:** Reset System Configuration is destructive to the host configuration and should not be a routine first troubleshooting step. Inspect the disk/controller, ESXi storage devices, partitioning, VMFS datastore creation/mounting, and host refresh/rescan before considering a reset. The instructor's attribution to a specific Workstation version is not verified here.

### 4. Online Practice Labs and Certification Exams (Source lines 73–97)

**Speaker 1 (Instructor):** Now, what are we going to do today? First, we will begin the virtual machine chapter.

**Anshul Saini:** Sir, there are online VMware labs. Could we practice there? For example, if access to the KR lab is difficult next week because of timing, can we use those online labs?

**Speaker 1 (Instructor):** Yes, certainly. You can try them, but first see what limitations they have. These are VMware virtual labs.

**Speaker 1 (Instructor):** Microsoft also offers labs of this kind. You can practice the fundamentals there. VMware followed a similar approach. However, one limitation with these guided web-based labs is that not every control or click is available.

**Speaker 1 (Instructor):** For example, suppose the lab is specifically about deploying storage. The steps that belong to storage deployment work, but other controls may be disabled. It is like a simulated or restricted website where only the prescribed actions can be taken.

**Speaker 1 (Instructor):** You cannot necessarily do everything you would do in a fresh environment: install a complete ESXi host, enable or disable arbitrary services, or freely navigate every setting. Your access is limited by the exercise.

**Speaker 1 (Instructor):** Suppose you are doing a virtual-machine creation lab and you click Storage. It might allow the first click but not show anything useful, or it might show something that you cannot click further. This is one of the limitations.

**Participant:** Okay. Does the certification exam work like that? Can they test these tasks there?

**Speaker 1 (Instructor):** Pearson VUE conducts many global certification exams. People take examinations for Microsoft, networking, VMware, and other certifications using testing providers. In the past, Pearson VUE and Prometric were names you might hear.

**Speaker 1 (Instructor):** In a scenario-based exam you might be given a simulated environment or interface with a particular service failure and be asked to troubleshoot. Only the relevant parts of the interface may be usable, rather than every possible option.

**Participants:** Okay, understood. Yes, sir.

> **Editorial note:** Certification exam delivery, supported providers and simulation formats depend on the specific exam and current vendor policies; the statements above reproduce the instructor's discussion, not a universal rule.

### 5. Beginning the Virtual Machine Chapter (Source lines 98–118)

**Speaker 1 (Instructor):** Today's chapter is both interesting and important: virtual machines. Before we create a virtual machine, let's recall what we built earlier.

**Participant:** Sir, your voice is lagging or breaking up.

**Speaker 1 (Instructor):** It may be the network. Let me switch networks and check. Hello, hello. Is my voice coming through properly now?

**Participants:** Yes, sir, it is working now.

**Speaker 1 (Instructor):** I think my core network is having some issues. It was working last night, around 11 or 12, but this morning it is behaving differently. Let me cross-check. Okay, let's continue.

**Speaker 1 (Instructor):** In the last class, we created a software-based data center. Can everyone see my screen?

**Participants:** Yes, sir, the screen is visible.

**Speaker 1 (Instructor):** After creating the data center, we added our ESXi hosts. We also built a cluster. Why did we create a cluster? One reason was to use DRS, the feature we examined previously.

**Speaker 1 (Instructor):** For example, suppose an ESXi host has very high utilization. Some of the virtual machines running on that host might not have sufficient CPU or memory. In the cluster, DRS can help move suitable virtual machines to another host with available resources.

**Speaker 1 (Instructor):** We also looked at High Availability. If an ESXi host goes down because of a power failure or another fault, HA helps get the affected virtual machines running again on available hosts in the cluster.

**Speaker 1 (Instructor):** Those are some of the most useful cluster features, which is why we created the cluster. In addition, we created a VMware storage solution called vSAN. Previously, we had used network-attached or SAN storage. vSAN is another VMware capability that we can use.

**Speaker 1 (Instructor):** The next step is to create virtual servers in this infrastructure. We have ESXi hosts for CPU and memory, and we have storage options. We must now consider the resources needed to create and operate a virtual machine.

> **Translation boundary:** Part 01 stops after original line 118. The resource-by-resource VM explanation and distributed-switch demonstration continue in the later portions of the original recording. No claim is made that the remaining lecture has been fully translated in this file.
