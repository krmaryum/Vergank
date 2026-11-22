# Day 03 Part A — VMware Tools verification, performance and student questions

**Original-source reference:** A:79–128.

**Instructor (A:79–83):** After restarting the guest, look at the result. The display now occupies the available window; resizing VMware Workstation also resizes the guest resolution. I ask whether anyone has created virtual machines before. A participant explains that they have deployed Linux and Windows in VirtualBox, not VMware. People naturally prefer tools they already know, but Workstation adds integration and networking capabilities worth exploring.

**Student (A:84):** Sir, people say VMware is heavy while VirtualBox is lightweight. What does that mean?

**Instructor (A:85–92):** Applications with more features can run more supporting services and therefore consume different amounts of CPU and RAM. Monitor the actual usage with Task Manager rather than relying only on reputation. Think back to Windows XP and Windows Server 2003, when people discussed machines with 64, 128, 256 or 512 MB of RAM. Modern software and hardware expectations are very different, even compared with inexpensive smartphones.

**Instructor (A:93–103):** We discussed Windows Server installation with Desktop Experience versus Server Core and the difference between a minimum requirement and resources appropriate for good performance. The instructor mentions small example RAM allocations and 4–8 GB for a usable lab, while noting that installed services and applications determine the real requirement. Having 8–16 GB on a host and SSD-based storage can make small virtual labs comfortable; slower disks, CPU contention and concurrent VMs can cause delays. The instructor relates this to his tower machine and a second-hand laptop used for previous classes.

**Student (A:109–110):** Last time I used VMware I encountered trouble, but the copy I received this time works. Did I simply not know how to use it before?

**Instructor (A:111–128):** Not necessarily. Different releases, operating-system compatibility and hardware behavior can explain the discrepancy. The instructor uses the analogy of buying a new motorcycle: when you chose it yourself, you are more willing to learn its quirks. Older Workstation versions 15 and 16 behaved differently in some configurations. Back in the demonstration, the VM is logged in and resizing correctly. Pressing Ctrl+Alt returns control to the host.
