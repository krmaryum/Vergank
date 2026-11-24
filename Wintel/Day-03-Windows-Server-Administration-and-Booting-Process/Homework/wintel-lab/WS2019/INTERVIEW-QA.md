# Interview Questions and Answers: Windows Server 2019 Installation

**Language:** English | [Roman Urdu](INTERVIEW-QA.roman-urdu.md)  ·  Back to the [guide](README.md)

25 beginner-level questions you could be asked in a help desk, junior sysadmin or IT support interview, based on this lab.

**How to practice:** Cover the answer, say your answer **out loud**, then compare. Interviewers like short, clear answers followed by one real example ("In my lab, I...").

## Contents

- [Windows Server 2019 basics](#windows-server-2019-basics) (Q1 to Q7)
- [Installation](#installation) (Q8 to Q13)
- [Virtual machines and VMware](#virtual-machines-and-vmware) (Q14 to Q20)
- [Firmware and boot](#firmware-and-boot) (Q21 to Q22)
- [After installation](#after-installation) (Q23 to Q25)

---

## Windows Server 2019 basics

### Q1. What is Windows Server, and how is it different from Windows 10?
**Answer:** Windows Server is Microsoft's operating system for **servers**: computers that provide services to other computers, like logins, file sharing, websites or DNS. Windows 10 is a **client** OS for one person's daily use. Server adds **roles** (like Active Directory, DNS, DHCP, File Services), supports many users at once, and is licensed differently.

### Q2. What editions of Windows Server 2019 are there?
**Answer:** The main ones are **Essentials** (small businesses, up to 25 users), **Standard**, and **Datacenter**. Standard and Datacenter have the same core features; Datacenter adds advanced features and unlimited virtualization rights.

### Q3. What is the difference between Standard and Datacenter?
**Answer:** A **Standard** license lets you run **2** Windows Server virtual machines on the licensed host. **Datacenter** allows **unlimited** Windows Server VMs and adds features like **Storage Spaces Direct**, **Shielded VMs** and full **Storage Replica**. Datacenter is for heavily virtualized environments. *In my lab I installed Datacenter Evaluation so I could try every feature.*

### Q4. What is the difference between Server Core and Desktop Experience?
**Answer:** **Desktop Experience** has the full graphical desktop (Start menu, File Explorer, Server Manager). **Server Core** has **no desktop**, only a command window; you manage it with PowerShell, `sconfig`, or remotely from another computer. Server Core uses less disk and RAM, needs fewer updates, and has a **smaller attack surface** (fewer things to hack). In Server 2019 you choose this during setup, and you can't switch later without reinstalling.

### Q5. Why would a company choose Server Core?
**Answer:** It is **more secure** (less software to attack), **needs fewer restarts** for updates, and uses **fewer resources**. Most servers are managed remotely anyway, so the desktop is often not needed.

### Q6. What are the minimum hardware requirements for Windows Server 2019?
**Answer:** A **1.4 GHz 64-bit** processor, **512 MB RAM** for Server Core (**2 GB** for Desktop Experience), and **32 GB** of disk space. In practice you should give it more. *In my lab I used 2 cores, 4 GB RAM and an 80 GB disk.*

### Q7. What is an evaluation version, and how long does it last?
**Answer:** It is the full product, free to try, for **180 days**. You install it without a product key. After 180 days it starts shutting down regularly until you activate it. It is perfect for labs and testing. An evaluation can be converted to a licensed version with a valid key.

---

## Installation

### Q8. What is an ISO file?
**Answer:** A single file that is an exact **image of a DVD**. In a VM, you attach the ISO to the virtual CD/DVD drive and the VM boots from it as if it were a real disc.

### Q9. What is the difference between a Custom and an Upgrade installation?
**Answer:** **Upgrade** keeps files, settings and apps from an older Windows already on the disk. **Custom (clean install)** installs a fresh copy on an empty or formatted partition. For a new server, you choose **Custom**.

### Q10. What does "Unallocated Space" mean on the disk selection screen?
**Answer:** The disk has **no partitions**: it is empty and not formatted. If you select it and click Next, Setup automatically creates the partitions it needs (system, recovery, and the main Windows partition) and formats them with **NTFS**.

### Q11. What are the password rules for the Administrator account?
**Answer:** By default, Windows Server requires a **complex password**: at least **8 characters**, using characters from **3 of 4 groups**: upper case, lower case, numbers, symbols. It also can't contain the user name.

### Q12. Why should you not install a server with the default time zone?
**Answer:** Setup defaults to **Pacific Time**. A wrong time zone causes wrong timestamps in logs, and in a domain, **Kerberos authentication fails if clocks differ by more than 5 minutes**. *In my lab the VM was 2 hours behind the host until I fixed the time zone.*

### Q13. You press Ctrl+Alt+Del in a VMware VM and the host's menu opens. Why, and what do you do?
**Answer:** The **host** OS always captures Ctrl+Alt+Del. In VMware Workstation you press **Ctrl+Alt+Insert**, or use **VM > Send Ctrl+Alt+Del**.

---

## Virtual machines and VMware

### Q14. What is a virtual machine?
**Answer:** A **software computer** that runs on a real computer. It has its own virtual CPU, memory, disk and network card, and runs its own operating system. Several VMs can run on one physical machine, isolated from each other.

### Q15. What is a hypervisor? What are the two types?
**Answer:** A hypervisor is the software that creates and runs VMs.
- **Type 1 (bare-metal)** runs directly on the hardware, with no OS underneath. Examples: **VMware ESXi**, **Microsoft Hyper-V**. Used in data centers.
- **Type 2 (hosted)** runs as an application on top of a normal OS. Examples: **VMware Workstation**, **VirtualBox**. Used for labs and testing.

### Q16. What is the difference between a host and a guest?
**Answer:** The **host** is the real computer running the hypervisor. The **guest** is the OS running inside the VM. *In my lab: host = Windows 10 Pro, guest = Windows Server 2019.*

### Q17. Explain Bridged, NAT and Host-only networking.
**Answer:**
- **Bridged:** the VM is connected directly to the physical network and gets its **own IP** from the real router, like another PC on the network.
- **NAT:** the VM shares the **host's IP address**. It can reach the internet, but other devices can't easily reach it.
- **Host-only:** the VM can only talk to the **host** and other host-only VMs. No internet.

*I used Bridged because a server should be reachable by other computers on the network.*

### Q18. What is VMware Tools, and why install it?
**Answer:** A package of **drivers and services** for the guest OS. It gives better video (screen resizing), smooth mouse movement, copy/paste between host and guest, better network and disk performance, and **time sync**. It should always be installed in a VMware VM.

### Q19. What is the difference between a thin-provisioned disk and a split disk?
**Answer:** **Thin provisioning** means the disk file **starts small and grows** as data is written, up to the maximum size (e.g. 80 GB). **Split** means the disk is stored as **many smaller files** instead of one big file, which makes it easier to copy and move. In Workstation, a disk can be both.

### Q20. What is a snapshot, and is it a backup?
**Answer:** A snapshot saves the **state of a VM at a point in time** so you can go back to it later. It is **not** a real backup, because it depends on the original disk files: if those are lost or damaged, the snapshot is useless too. Snapshots are great before risky changes, but should not be kept for a long time.

---

## Firmware and boot

### Q21. What is the difference between BIOS and UEFI?
**Answer:** Both are **firmware** that starts the computer before the OS.
- **BIOS** (Legacy) is older, uses **MBR** disks (max **2 TB**, max 4 primary partitions), and has no Secure Boot.
- **UEFI** is newer, uses **GPT** disks (much larger than 2 TB, up to 128 partitions in Windows), boots faster, and supports **Secure Boot**, which blocks untrusted boot software.

Modern servers and Windows 11 use UEFI.

### Q22. Your VM shows a UEFI Boot Manager screen instead of Windows Setup. What do you do?
**Answer:** With UEFI, the Windows ISO waits only a few seconds for "Press any key to boot from CD or DVD". If it is missed, the VM drops to the Boot Manager. Fixes: restart the VM, **click inside it quickly and press a key**; or use **Power On to Firmware** and choose the CD/DVD; or, **before the OS is installed**, change the firmware to **BIOS** in VM Settings > Options > Advanced. *In my lab I switched to BIOS and Setup started straight away.* Never change firmware after installing, or the VM may not boot.

---

## After installation

### Q23. What is Server Manager?
**Answer:** The main **graphical management console** in Windows Server. It opens at login and lets you add **roles and features**, view events and services, configure the local server (name, IP, updates), and manage other servers.

### Q24. What is the difference between a role and a feature?
**Answer:** A **role** is a main job the server does for others, like **AD DS**, **DNS**, **DHCP**, **File and Storage Services** or **Web Server (IIS)**. A **feature** is a supporting tool, like **.NET Framework**, **Windows Server Backup** or **Telnet Client**. Both are added with **Add Roles and Features** in Server Manager (or `Install-WindowsFeature` in PowerShell).

### Q25. What are the first things you configure after installing a new server?
**Answer:**
1. Install **VMware Tools** (if it is a VMware VM) or other drivers.
2. Set the correct **time zone** and time.
3. **Rename** the computer to a meaningful name.
4. Give it a **static IP address** and correct **DNS** settings.
5. Run **Windows Update**.
6. Take a **snapshot** or backup before adding roles.
7. Then add roles, for example join a domain or promote it to a domain controller.

---

**Bonus question:** *When does support end for Windows Server 2019?*
Mainstream support ended on **9 January 2024**. Extended support (security updates only) runs until **9 January 2029**. Server 2019 is a **Long-Term Servicing Channel (LTSC)** release, built on the same code base as Windows 10 version 1809.

**Bonus question 2:** *What is Windows Admin Center?*
A free, **browser-based** management tool from Microsoft. You install it once on a server or PC, then manage many servers from a web browser. It is the modern partner to Server Manager. Server Manager in 2019 shows a pop-up suggesting it; you can safely tick "Don't show this message again".
