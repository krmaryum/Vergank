# Wintel Day 02 — Part 06: Home Lab Decisions and Choosing Windows Server Installation Media

**Source alignment:** Original `Wintel-day-02.txt`, lines 355–429. **Editorial type:** Source-grounded, rewritten classroom dialogue; **not a line-by-line or verbatim translation**. Refer to `Original_Source/` for every original utterance. Speaker names in the source are sometimes inaccurate.

## Classroom discussion

**Instructor:** Let us connect enterprise concepts with the lab you can actually build. Not every student has access to a data center, and some people practice from overseas. A physical server may be expensive, noisy, or difficult to maintain at home. Depending on the exercise, a laptop or desktop with sufficient resources can host multiple virtual machines and let you practice Windows Server and related services.

**Instructor:** Khalid is particularly interested in the hardware requirements because he is trying to build a personal lab. We discuss buying new versus used equipment, resource limits, and the importance of a setup that can support the actual class exercises. For smaller demonstrations, the memory requirement may be modest; more complex concurrent VMs need additional RAM and CPU capacity.

**Instructor:** Another decision is whether to install Windows Server directly on a physical computer or inside a virtual machine. Direct installation can encounter hardware and driver compatibility problems on consumer laptops and desktops. The class therefore uses VMware Workstation for a controlled training environment. Instead of changing the host OS, students can create a VM and attach a Windows Server ISO.

**Instructor:** I have a shared folder containing operating-system installers, the VMware Workstation installation files, and additional course materials. Get the required software from the provided training location. Before using an installer, verify the source, edition, compatibility, integrity, and licensing for your lab. A file in a shared folder is not automatically safe or properly licensed.

**Instructor:** The goal is to be able to repeat the exercises independently. During the class I show Windows performance and hardware details so students can identify how much RAM, CPU, and storage they have before allocating resources to VMs.
