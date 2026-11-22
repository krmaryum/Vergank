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
