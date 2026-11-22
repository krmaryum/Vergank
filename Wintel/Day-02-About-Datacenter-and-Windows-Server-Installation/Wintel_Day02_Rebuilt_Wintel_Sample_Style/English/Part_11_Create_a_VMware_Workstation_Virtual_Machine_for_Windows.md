# Wintel Day 02 — Part 11: Create a VMware Workstation Virtual Machine for Windows Server

**Source alignment:** Original `Wintel-day-02.txt`, lines 741–810. **Editorial type:** Source-grounded, rewritten classroom dialogue; **not a line-by-line or verbatim translation**. Refer to `Original_Source/` for every original utterance. Speaker names in the source are sometimes inaccurate.

## Classroom discussion

**Instructor:** Let's create a virtual machine in VMware Workstation. Think of the virtual machine as a computer whose CPU, RAM, disks and network adapters are implemented as virtual hardware on a host. The first task is to launch the new-VM wizard and decide how installation media will be supplied.

**Instructor:** The wizard may offer a physical CD/DVD device or an ISO file. We are using an ISO. Then select the appropriate guest operating-system family and version. The operating system selection matters because VMware uses it to choose suitable default settings and virtual hardware behavior.

**Instructor:** Next come the resources. Choose virtual processor settings, memory capacity and a virtual disk. The instructor uses a Windows Server example and allocates a disk for the OS. Another virtual disk can later be added for application or user data. Keeping OS and data volumes logically separate can make administration and future lab demonstrations easier.

**Instructor:** These choices must fit the physical host. A VM does not create unlimited physical memory. Allocating far more resources than the host can support can make both the guest and the host perform badly. The virtual networking mode also determines how the guest reaches other systems.

**Instructor:** Finally, review the configuration before creating the VM. You are not merely clicking Next; you should be able to explain what the ISO, virtual CPU, RAM, disk and virtual NIC each contribute.
