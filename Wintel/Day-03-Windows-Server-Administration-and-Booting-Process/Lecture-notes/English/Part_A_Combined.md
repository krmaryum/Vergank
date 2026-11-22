# Day 03 — Part A: Classroom English Translation

## Section 1 — Review of previous lessons and selection of the lab hypervisor

**Instructor (source A:1–3):** What do companies do, and why do some of them have thousands upon thousands of servers? What are the business requirements? What are projects, how are projects carried out, and what are tickets? When you go through these sessions, you will recognize how these things fit together. You may already have worked in application technical support. Here, we are approaching the same concepts from a server and infrastructure perspective.

**Instructor (A:4–5):** You already know concepts such as SLAs and P1, P2 and P3 tickets, right? We discussed related subjects on Day 01.

**Instructor (A:6–9):** In Day 02, we discussed operating systems, work performed on servers, and the components of a data center: routing, switching, networking devices, storage, power infrastructure and the different kinds of servers. We also saw how we can deploy Windows Server in a lab on our laptop or desktop. We cannot expect everyone to purchase a dedicated physical server just for training.

**Instructor (A:10–12):** Yesterday we deployed Windows Server 2022. We can also deploy Windows Server 2025; its installation process is broadly similar. In the next class we can have Server 2025 deployed as well. First, I will power on the server from yesterday. We are using VMware Workstation as the virtualization platform for the lab.

**Instructor (A:13–18):** Why are we not using Microsoft Hyper-V yet? Because we have not studied Hyper-V. If I introduce Hyper-V concepts at the beginning, some of the terminology may be confusing. We will study the Hyper-V role and how to install it later. For now, we will use VMware Workstation. It is a third-party application, not a Microsoft product, and the edition we are using is available without an additional fee.

**Student (A:19):** Sir, what is the difference between VirtualBox and VMware?

**Instructor (A:19–28):** VirtualBox is made by Oracle. VMware previously offered VMware Player and VMware Workstation as different products. Workstation Pro used to be licensed as a paid product. We are now using a newer Workstation version, which the instructor identifies as 26H1 after briefly considering its version number. My approach is not necessarily to adopt the newest release immediately. A slightly older, reliable version can be preferable if you are concerned about unknown issues.

**Instructor (A:29–34):** Workstation offers features such as snapshots and advanced virtual networking. I also have a YouTube playlist covering VMware Workstation, including the networking chapter. I find Workstation feature-rich and easier to use than the alternatives, including Hyper-V, for this training. That last comparison is my experience and preference.

## Section 2 — Why VMware Tools is installed after Windows Server

**Instructor (A:35–38):** We installed Windows Server in VMware Workstation yesterday. When you log in after installing the operating system, the graphics or display resolution may not look very good. A server OS is not primarily designed to provide the same desktop appearance as Windows 10 or 11. Additionally, the virtual machine may not yet have the integration components and drivers used by VMware Tools.

**Instructor (A:39–44):** VMware Workstation is a Type 2 hypervisor. We also work with Type 1 hypervisors in production environments, including the VMware material covered in another batch. We will explore Type 1 versus Type 2 more thoroughly when studying Hyper-V. For a Windows guest running in VMware, we should install VMware Tools to enable guest-integration features.

**Instructor (A:45–47):** Look at this VM window. I am making it full-screen, but there are black areas on the left and right, and the Windows Start button stays inside a smaller display. The guest screen has not resized to fit the available window.

**Instructor (A:48–49):** Consider a file on the host computer's desktop. You might want to copy it into the guest virtual machine. VMware Tools can provide integration features that make copying and pasting easier when the relevant settings are enabled. Right now, that functionality is not available in this demonstration because the tools are not installed.

**Instructor (A:50–56):** Today, the first task is installing VMware Tools. After creating a Windows guest, I recommend checking the tools installation. There may be a notification at the bottom saying that VMware Tools are not installed. You can click that notification, right-click the VM tab, or open the **VM** menu and select **Install VMware Tools**.

**Instructor (A:57–62):** When you select that command, the VMware Tools installer media is connected to the VM as a virtual ISO. Return to the Windows guest. You may see an AutoPlay pop-up, or you can open **This PC**, find the attached virtual DVD, and launch the installer. If necessary, right-click the setup program and choose **Run as administrator**.

**Instructor (A:63–68):** In the installation wizard, I am selecting the **Complete** option rather than **Typical**, because I want the full package of components for this demonstration. Then I click Next and Install. The process takes a few minutes and will request a restart.

**Instructor (A:69–77):** This brings us back to an operational concern we discussed: a new server build should occur inside an approved maintenance or change window. A company might allocate four, six or eight hours. During that approved period, we can perform the planned reboots. But rebooting a production server without authorization can trigger an escalation. We may need a Root Cause Analysis (RCA) explaining the incident and how to prevent a recurrence. In our lab this is a planned activity, so we can reboot now.

**Instructor (A:78):** After the restart, the VM should resize more effectively when I change the size of the VMware Workstation window.


---

# Day 03 Part A — VMware Tools verification, performance and student questions

**Original-source reference:** A:79–128.

**Instructor (A:79–83):** After restarting the guest, look at the result. The display now occupies the available window; resizing VMware Workstation also resizes the guest resolution. I ask whether anyone has created virtual machines before. A participant explains that they have deployed Linux and Windows in VirtualBox, not VMware. People naturally prefer tools they already know, but Workstation adds integration and networking capabilities worth exploring.

**Student (A:84):** Sir, people say VMware is heavy while VirtualBox is lightweight. What does that mean?

**Instructor (A:85–92):** Applications with more features can run more supporting services and therefore consume different amounts of CPU and RAM. Monitor the actual usage with Task Manager rather than relying only on reputation. Think back to Windows XP and Windows Server 2003, when people discussed machines with 64, 128, 256 or 512 MB of RAM. Modern software and hardware expectations are very different, even compared with inexpensive smartphones.

**Instructor (A:93–103):** We discussed Windows Server installation with Desktop Experience versus Server Core and the difference between a minimum requirement and resources appropriate for good performance. The instructor mentions small example RAM allocations and 4–8 GB for a usable lab, while noting that installed services and applications determine the real requirement. Having 8–16 GB on a host and SSD-based storage can make small virtual labs comfortable; slower disks, CPU contention and concurrent VMs can cause delays. The instructor relates this to his tower machine and a second-hand laptop used for previous classes.

**Student (A:109–110):** Last time I used VMware I encountered trouble, but the copy I received this time works. Did I simply not know how to use it before?

**Instructor (A:111–128):** Not necessarily. Different releases, operating-system compatibility and hardware behavior can explain the discrepancy. The instructor uses the analogy of buying a new motorcycle: when you chose it yourself, you are more willing to learn its quirks. Older Workstation versions 15 and 16 behaved differently in some configurations. Back in the demonstration, the VM is logged in and resizing correctly. Pressing Ctrl+Alt returns control to the host.


---

# Day 03 Part A — Server Manager, auto-start and Internet Explorer

**Original-source reference:** A:129–153.

**Instructor (A:129–136):** VMware Tools gives us host–guest integration, and now we turn to the Windows Server administrative interface. Server Manager usually appears after login. It is more than a welcome screen: it is an entry point for server status, roles, and administration.

**Instructor (A:137–147):** Server Manager provides status indicators and alerts. If you prefer not to have it open automatically at every logon, configure its auto-start setting. This does not remove Server Manager; it simply prevents the automatic opening of the console. You can launch it yourself whenever required.

**Instructor (A:148–153):** Minimizing a window is not the same as controlling whether it launches at sign-in. Understand what is running and why. The instructor then begins a discussion of legacy Internet Explorer and the security implications of old applications during vulnerability reviews.


---

# Day 03 Part A — Vulnerability scanning, Defender and centralized antivirus

**Original-source reference:** A:154–194.

**Instructor (A:154–161):** Organizations conduct security audits and vulnerability scans. Legacy Internet Explorer or another outdated component can generate a vulnerability finding. The instructor mentions using a short PowerShell script for checking or managing such components. The exact script was not transcribed, so no command is invented here; production use requires testing and authorization.

**Instructor (A:162–172):** Does a newly installed Windows Server need additional antivirus software? The instructor directs attention to Microsoft Defender, which is built into supported Windows Server versions. But a company's actual protection stack depends on policy, licensing, threat detection and management. He talks about the general behavior of scanning and the detection of a suspicious file.

**Instructor (A:173–181):** Organizations may also use SentinelOne, Norton or another endpoint security product. Many such agents are managed through a centralized portal. Administrators may be able to review onboarding, alerts and scan status there. Uninstalling a centrally managed agent may require removing the device assignment or providing an approved authorization; local admin rights alone may not be enough.

**Instructor (A:182–194):** With the correct permissions, teams can manage applicable policies and scan controls. Enterprises also use cloud management for mobile and remote endpoints, subject to subscriptions and company policy. Installing the operating system is only the beginning: validate the actual protection state and applicable management procedures.


---

# Day 03 Part A — Windows Defender Firewall, profiles, rules and student question

**Original-source reference:** A:195–231.

**Instructor (A:195–204):** We open the Windows Defender Firewall interface, including by entering `firewall.cpl` in Run. Look at the firewall profiles and current state. The instructor points to the status indicator and notes that the firewall is often enabled by default. Before changing any production security setting, assess the business need and impact.

**Instructor (A:205–213):** The interface offers controls to turn the firewall on or off. The option to block all incoming connections, including allowed applications, can prevent legitimate connectivity too. More granular inbound and outbound controls are available in the advanced firewall console; disabling protection wholesale is not the preferred way to permit a service.

**Instructor (A:214–226):** Enterprise teams may use centralized security products, network controls and group policies. An apparently disabled host firewall is not enough evidence to assume adequate protection; understand the company's actual design. For client-server communication, identify required ports and configure narrowly scoped exceptions.

**Student / Instructor (A:227–231):** Sarfraz asks how a file server can function when the firewall remains enabled. The conversation returns to managing appropriate rules through Group Policy. The student acknowledges that his question has been answered.


---

# Day 03 Part A — Enterprise readiness, PAM and server auditing

**Original-source reference:** A:232–273.

**Instructor (A:232–241):** I ask whether the class pace is appropriate or the material is going over anyone's head. The goal is not merely to click through an installation wizard. Enterprise administration also involves approvals, operational handover, security, permissions, and monitoring. A technician who can install an OS may still be unfamiliar with the procedures needed in a live data center.

**Instructor (A:242–253):** A recurring problem is uncontrolled use of highly privileged accounts. Organizations may use a Privileged Access Management (PAM) tool. Instead of handing out shared static passwords, a managed vault can issue, rotate, or control access to credentials.

**Student / Instructor (A:249–257):** Why have a tool generate a password when an administrator could create one manually? The instructor explains that the benefit goes beyond generating a string: approved access, rotation, session control and accountability. Having a normal Active Directory account is not necessarily the same as being authorized for privileged activity on a particular server.

**Instructor (A:258–264):** Some PAM systems record privileged sessions or provide audit trails. If an administrator reboots a server and later disputes doing so, the organization can investigate the actual approved session evidence. Such monitoring should still follow security and privacy policies.

**Instructor (A:265–273):** The instructor also describes making notes whenever a useful idea occurs during teaching. Unexpected troubleshooting should be treated as an opportunity to learn, rather than something to fear.


---

# Day 03 Part A — Student AI questions, Python and automation examples

**Original-source reference:** A:274–323.

**Instructor (A:274–283):** Information is increasingly accessible through search engines, technical documentation and AI assistants. I encourage students to learn how to ask useful prompts and evaluate the responses rather than accepting a single answer blindly. We discuss ChatGPT, Claude and Gemini as examples.

**Instructor (A:284–297):** Comparing how different tools explain a question can reveal another route to a solution. Share useful findings with classmates, but keep the WhatsApp study group professional and focused; irrelevant chatter makes it harder to find important technical posts.

**Student (A:298–303):** I gave a coding problem to ChatGPT and Claude. In my case Claude's free version explained the Python code more effectively than the paid tool I was using. I am comparing their coding assistance, not making an absolute claim about every task.

**Instructor (A:303–316):** I am also working on automation. Previously my student registration workflow involved manual emails, WhatsApp messages and calls. The idea is to trigger follow-up messages automatically when someone submits registration. I discuss experimenting with Azure and Meta integration instead of relying entirely on external automation platforms. AI can suggest different ways to design such a workflow.

**Instructor (A:317–323):** Use AI thoughtfully for scripting, searching, documentation and troubleshooting—not simply for editing pictures. Validate every command before using it in a production environment.


---

# Day 03 Part A — DHCP scripts, IP leases and shortcut techniques

**Original-source reference:** A:324–350.

**Instructor (A:324–333):** Upcoming lessons will introduce practical scripts, including DHCP-related administration. A DHCP server assigns IP addresses from a pool with lease periods. Administrators may encounter old leases, bad-address records or pool exhaustion, especially at scale. Automation can help investigate such cases, although the transcript does not provide a specific full script to reproduce here.

**Instructor (A:334–340):** The instructor emphasizes professional communication while remaining approachable to students. We have installed VMware Tools and explored basic server administration; we are now approaching the shutdown demonstration.

**Instructor (A:341–350):** VMware Tools improves guest display and integration. We also discuss keyboard shortcuts for moving between host and guest controls and for common administrative tasks. The instructor promises to identify shortcuts when using them, since small efficiencies can save time during routine work.


---

# Day 03 Part A — Windows Server shutdown reason and planned downtime

**Original-source reference:** A:351–369.

**Instructor (A:351–356):** I press `Alt+F4` on the Windows Server desktop and open the shutdown dialog. Windows Server can prompt for a shutdown reason. Unlike casually turning off a personal laptop, shutting down a server may interrupt services that other people rely on, so the operation should be intentional and authorized.

**Instructor (A:357–363):** Planned maintenance, hardware work, OS recovery, or storage reconfiguration can require a shutdown. Recording the reason improves operational traceability. The instructor compares how the shortcut and shutdown UI work on a Windows Server VM versus guests in an ESXi environment.

**Instructor (A:364–369):** Accidental shutdowns also happen. Appropriate permissions, approvals, team communications, rollback plans and service verification reduce the impact of mistakes.


---

# Day 03 Part A — Real incident: accidental shutdown, audit, RCA and PIP

**Original-source reference:** A:370–421.

**Instructor (A:370–379):** The instructor describes a real project incident. A night-shift technician received a ticket and logged on to a server. Although the task was essentially L1 work, the team's access arrangements allowed higher privileges in some cases. While finishing the work, the technician shut down the server by mistake. It was brought back online a few minutes later, but that still constituted customer-visible downtime.

**Instructor (A:380–389):** The client sent an email the next day. The instructor had to establish when the server was powered off, who performed the action and what happened. Available audit and session-recording tools helped review the event. He spoke to the employee and prepared incident communication and an RCA. Five minutes of outage is not automatically insignificant in a production environment.

**Instructor (A:390–399):** The situation became more difficult when someone on the next shift failed to read WhatsApp, Teams and email updates. The instructor introduces the importance of shift handovers and daily huddles. Teams must communicate outstanding incidents, approved changes and unresolved tasks so that problems are not repeated or mishandled.

**Instructor (A:400–415):** Management may discuss corrective action or a Performance Improvement Plan (PIP). The instructor shares personal opinions about personnel management; these are not universal HR rules. The operational takeaway is to treat mistakes seriously, document evidence, communicate clearly and improve processes rather than hiding the issue. New and experienced administrators alike can make mistakes.

**Instructor (A:416–421):** Technical commands alone do not define a good enterprise administrator. Responsibility, communication, approvals and accountability matter just as much.


---

# Day 03 Part A — International calling question, break and closing discussion

**Original-source reference:** A:422–453.

**Instructor / Student (A:422–438):** Toward the end of the recording, the instructor and Sarfraz discuss a phone-call problem. Calls initiated by the instructor do not connect, although incoming calls from Sarfraz can arrive. They check whether the number has the Indian country code `+91` or `0091` correctly saved. Rather than spending money on international calls, they agree Teams or WhatsApp calling is a practical alternative.

**Instructor / Students (A:439–453):** The instructor proposes a ten-minute break before continuing. Participants also discuss the time difference between their locations—morning for some and evening or night for others. The instructor gives a further update and students acknowledge it. This ordinary conversation is retained as part of the classroom flow, rather than silently removed.
