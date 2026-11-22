# Day 03 Part B — Kernel, HAL, session manager, logon and SAM

**Source:** B:244–270

**Instructor / classroom discussion:** The instructor continues from the Windows loader to the kernel and Hardware Abstraction Layer (HAL). He discusses driver initialization, graphics, networking and device availability, then introduces smss.exe (Session Manager) and winlogon.exe in the Windows sign-in sequence. In a Windows system, he locates the local Security Accounts Manager hive at `C:\Windows\System32\config\SAM` as a demonstration. He connects account validation and LSASS to sign-in; the exact roles of NTLM, domain authentication and modern Windows components are explained separately in technical notes. Students ask whether their answer should describe BIOS or UEFI. He says it should match the machine's actual configuration. Rufus, MBR/GPT and UEFI boot media are discussed as related deployment concepts.
