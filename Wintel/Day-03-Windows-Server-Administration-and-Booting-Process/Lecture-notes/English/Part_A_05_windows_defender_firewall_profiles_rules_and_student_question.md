# Day 03 Part A — Windows Defender Firewall, profiles, rules and student question

**Original-source reference:** A:195–231.

**Instructor (A:195–204):** We open the Windows Defender Firewall interface, including by entering `firewall.cpl` in Run. Look at the firewall profiles and current state. The instructor points to the status indicator and notes that the firewall is often enabled by default. Before changing any production security setting, assess the business need and impact.

**Instructor (A:205–213):** The interface offers controls to turn the firewall on or off. The option to block all incoming connections, including allowed applications, can prevent legitimate connectivity too. More granular inbound and outbound controls are available in the advanced firewall console; disabling protection wholesale is not the preferred way to permit a service.

**Instructor (A:214–226):** Enterprise teams may use centralized security products, network controls and group policies. An apparently disabled host firewall is not enough evidence to assume adequate protection; understand the company's actual design. For client-server communication, identify required ports and configure narrowly scoped exceptions.

**Student / Instructor (A:227–231):** Sarfraz asks how a file server can function when the firewall remains enabled. The conversation returns to managing appropriate rules through Group Policy. The student acknowledges that his question has been answered.
