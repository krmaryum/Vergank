# Day 03 Part A — Enterprise readiness, PAM and server auditing

**Original-source reference:** A:232–273.

**Instructor (A:232–241):** I ask whether the class pace is appropriate or the material is going over anyone's head. The goal is not merely to click through an installation wizard. Enterprise administration also involves approvals, operational handover, security, permissions, and monitoring. A technician who can install an OS may still be unfamiliar with the procedures needed in a live data center.

**Instructor (A:242–253):** A recurring problem is uncontrolled use of highly privileged accounts. Organizations may use a Privileged Access Management (PAM) tool. Instead of handing out shared static passwords, a managed vault can issue, rotate, or control access to credentials.

**Student / Instructor (A:249–257):** Why have a tool generate a password when an administrator could create one manually? The instructor explains that the benefit goes beyond generating a string: approved access, rotation, session control and accountability. Having a normal Active Directory account is not necessarily the same as being authorized for privileged activity on a particular server.

**Instructor (A:258–264):** Some PAM systems record privileged sessions or provide audit trails. If an administrator reboots a server and later disputes doing so, the organization can investigate the actual approved session evidence. Such monitoring should still follow security and privacy policies.

**Instructor (A:265–273):** The instructor also describes making notes whenever a useful idea occurs during teaching. Unexpected troubleshooting should be treated as an opportunity to learn, rather than something to fear.
