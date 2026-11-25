# Interview Questions and Answers: Windows Server 2022 Installation

**Language:** English | [Roman Urdu](INTERVIEW-QA.roman-urdu.md)  ·  Back to the [guide](README.md)

25 beginner-level questions you could be asked in a help desk, junior sysadmin or IT support interview, based on this lab. Questions about general VM basics are also in the [2019 Q&A](../WS2019/INTERVIEW-QA.md); this set focuses on **what is new in 2022** and on the steps of this lab.

**How to practice:** Cover the answer, say your answer **out loud**, then compare. Interviewers like short, clear answers followed by one real example ("In my lab, I...").

## Contents

- [Windows Server 2022 basics](#windows-server-2022-basics) (Q1 to Q8)
- [Installation](#installation) (Q9 to Q15)
- [Virtual machines and VMware](#virtual-machines-and-vmware) (Q16 to Q21)
- [After installation](#after-installation) (Q22 to Q25)

---

## Windows Server 2022 basics

### Q1. When was Windows Server 2022 released, and how long is it supported?
**Answer:** It was released in **August 2021** (build 20348). It is a **Long-Term Servicing Channel (LTSC)** release, which means 10 years of support: **mainstream support ended in October 2026**, and **extended support** (security updates only) runs until **October 2031**.

### Q2. What editions of Windows Server 2022 are there?
**Answer:** **Standard**, **Datacenter**, and **Datacenter: Azure Edition** (made to run in Microsoft Azure or on Azure Stack HCI). There is also **Essentials** for small businesses, sold only with new hardware. *In my lab I installed Standard (Desktop Experience).*

### Q3. What is the difference between Standard and Datacenter?
**Answer:** Both have the same core features. A **Standard** license allows **2** Windows Server VMs on the licensed host. **Datacenter** allows **unlimited** VMs and adds features like **Storage Spaces Direct**, **Shielded VMs** and **Software-Defined Networking**. Standard is for lightly virtualized or physical servers; Datacenter is for heavily virtualized data centers.

### Q4. Name some new features in Windows Server 2022.
**Answer:**
- **Secured-core server**: uses hardware security (TPM 2.0, Secure Boot, virtualization-based security) to protect against firmware attacks.
- **TLS 1.3** turned on by default, for safer network connections.
- **DNS over HTTPS (DoH)** client, so DNS lookups can be encrypted.
- **SMB AES-256 encryption** for file sharing, and **SMB over QUIC** (Azure Edition) for secure file access over the internet without a VPN.
- **Microsoft Edge** built in instead of Internet Explorer.
- Better **Azure hybrid** tools (Azure Arc, Windows Admin Center).

### Q5. What is the difference between Server Core and Desktop Experience?
**Answer:** **Desktop Experience** has the full graphical desktop (Start menu, Server Manager, File Explorer). **Server Core** has **no desktop**, only a command window; you manage it with PowerShell, `sconfig`, or remotely. Server Core is smaller, needs fewer updates, and has a **smaller attack surface**. You choose during Setup and can't switch later without reinstalling.

### Q6. What are the minimum hardware requirements for Windows Server 2022?
**Answer:** A **1.4 GHz 64-bit** processor, **512 MB RAM** for Server Core (**2 GB** for Desktop Experience), and **32 GB** of disk space. In practice give it more. *In my lab: 2 cores, about 4 GB RAM, 80 GB disk.*

### Q7. How can you tell if an ISO is the evaluation version?
**Answer:** The edition names in Setup include the word **"Evaluation"**, for example *Windows Server 2022 Standard Evaluation*. The evaluation runs for **180 days** without a key. *In my lab, the names did not say "Evaluation", so I knew it was a regular ISO that needs a product key to activate.*

### Q8. What happens if Windows Server is not activated?
**Answer:** It still installs and runs, and roles still work, but you see an **"Activate Windows"** watermark, some personalization settings are locked, and it is **not properly licensed**. For production, a server must always be activated with a valid license.

---

## Installation

### Q9. Why did you choose "I will install the operating system later" in VMware?
**Answer:** So VMware does not run **Easy Install**, which answers the Setup questions automatically. In a lab I want to see every Setup screen myself. I attached the ISO afterwards in **Customize Hardware**.

### Q10. Why did you change the firmware to BIOS, and when is it safe to do so?
**Answer:** With **UEFI**, the Windows ISO waits only a few seconds for "Press any key to boot from CD or DVD". If you miss it, the VM drops to the **Boot Manager**. That happened in my 2019 lab. **BIOS** boots the ISO straight away. It is safe to change **only before** Windows is installed, because BIOS and UEFI use different disk layouts (**MBR** vs **GPT**); changing it later can make Windows unbootable. *In my 2022 lab I switched to BIOS before the first boot and had no problem.*

### Q11. What is the difference between a Custom and an Upgrade installation?
**Answer:** **Upgrade** keeps files, settings and apps from an older Windows on the disk. **Custom** is a clean install on an empty or formatted disk. For a new server you choose **Custom**.

### Q12. What does "Unallocated Space" mean on the disk screen?
**Answer:** The disk has **no partitions** yet. When you select it and click Next, Setup creates the partitions it needs and formats them with **NTFS** automatically.

### Q13. The virtual disk is NVMe. Do you need to load a driver?
**Answer:** No. Windows Server 2022 has the **NVMe driver built in**, so the disk appears in Setup straight away. You only use **Load driver** for disk controllers Windows doesn't know.

### Q14. What are the password rules for the Administrator account?
**Answer:** A **complex password**: at least **8 characters**, with characters from **3 of 4 groups** (upper case, lower case, numbers, symbols), and it can't contain the user name.

### Q15. During Setup, the VM restarts and you see "Press any key to boot from CD or DVD". What do you do?
**Answer:** **Nothing.** Don't press a key. Setup wants to continue from the hard disk. Pressing a key would boot the ISO again and start Setup from the beginning.

---

## Virtual machines and VMware

### Q16. Why store the VM on D: and not in the default location?
**Answer:** The default is inside **OneDrive** on `C:`. OneDrive tries to sync every change to the cloud, and VM files are huge and constantly changing, so syncing is slow and can **corrupt** the VM. `D:` also had much more free space. *I stored it in `D:\VMs\WinSRV-2022`.*

### Q17. What does "Split virtual disk into multiple files" do?
**Answer:** It stores the virtual disk as many smaller files instead of one big file. Smaller files are easier to **copy, move and back up**. The disk is also **thin**: it starts small and grows as data is written.

### Q18. Why did you use Bridged networking?
**Answer:** **Bridged** puts the VM directly on the real network, with its **own IP address**, like another PC. A server should be reachable by other computers. **NAT** hides the VM behind the host's IP, and **Host-only** has no outside network at all.

### Q19. What is VMware Tools, and how do you know it is working?
**Answer:** A package of **drivers and services** for the guest: better display, smooth mouse, copy/paste, better network and disk performance, and time sync. You know it works when the **screen resizes** with the window, the mouse moves freely, and the menu shows **Reinstall VMware Tools**. *In my lab, the small screen filled the whole window after installing it.*

### Q20. VMware Tools: Typical or Complete?
**Answer:** **Typical** installs only what the current VMware product (Workstation) needs. **Complete** installs all features, useful if the VM may move to another VMware product like **ESXi**. *I chose Complete.*

### Q21. What is the yellow "I Finished Installing" bar in VMware?
**Answer:** A reminder VMware shows when you chose to install the OS later. Clicking **I Finished Installing** just tells VMware the install is complete and removes the bar. It doesn't change the VM.

---

## After installation

### Q22. Server Manager shows a red "Services" number. Is something broken?
**Answer:** Not necessarily. It counts services set to **Automatic** that are **not running**. On a new server this is common: some services start later (*Delayed Start*) or only when needed (*trigger start*), and some update services stop after finishing. I click **Services** to see which ones, refresh after a few minutes, and only start a service if it is really needed.

### Q23. Why check the time zone even if the clock looks correct?
**Answer:** The clock can look right today but be in the wrong zone, or miss **daylight saving** changes. In Active Directory, **Kerberos** fails if clocks differ by more than **5 minutes**. I set **(UTC-06:00) Central Time (US & Canada)**, not *Central America*, which has no daylight saving.

### Q24. What is the difference between a role and a feature?
**Answer:** A **role** is a main job the server does for others, like **AD DS**, **DNS**, **DHCP** or **IIS**. A **feature** is a supporting tool, like **.NET Framework** or **Windows Server Backup**. Both are added with **Add Roles and Features** in Server Manager or `Install-WindowsFeature` in PowerShell.

### Q25. What are the first things you configure after installing a new server?
**Answer:**
1. Install **VMware Tools** (or hardware drivers).
2. Check the **time zone**.
3. **Rename** the server.
4. Set a **static IP** and DNS.
5. Run **Windows Update**.
6. **Activate** Windows (if it is not an evaluation).
7. Take a **snapshot** or backup, then add roles.
