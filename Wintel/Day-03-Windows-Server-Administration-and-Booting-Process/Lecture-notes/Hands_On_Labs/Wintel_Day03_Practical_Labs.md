# Wintel Day 03 — Practical Labs

These are **additional suggested exercises**, not statements that all activities were demonstrated in the source recording. Work in a disposable VM; production changes require approval.

## Lab 01 — VMware Tools installation and verification
**Objective:** Observe the effect of guest tools on Windows Server display integration.

**Prerequisites:** A Windows Server guest running in VMware Workstation, with a restore point or VM snapshot.

1. Start the Windows Server VM and record the current resolution and guest-integration limitations.
2. In VMware Workstation choose **VM > Install VMware Tools**.
3. In the guest open **This PC**, launch the VMware Tools installer from the mounted virtual media and follow the wizard.
4. Restart the guest if prompted.
5. Resize the VM window and examine display changes; inspect VMware Tools in installed programs/services.

**Verify:** Screen resizing works and tools appear installed. Clipboard and file transfer depend on separate security settings.

**Troubleshoot:** If installer media does not mount, check virtual CD/DVD mapping and guest-tools installation state.

## Lab 02 — Server Manager inventory
**Objective:** Locate the local server settings and administration tools.

1. Log into Windows Server with an authorized administrator account.
2. Open **Server Manager** and review **Local Server**.
3. Record the computer name, Windows edition, Windows Update status, network adapter and Remote Desktop setting.
4. Review **Manage > Add Roles and Features** without installing unnecessary roles.

**Verify:** Produce a short inventory with the server name, OS version and network details.

## Lab 03 — Windows Firewall rule inspection
**Objective:** Inspect firewall profiles without weakening overall security.

1. Open **Windows Defender Firewall with Advanced Security**.
2. Check Domain, Private and Public profile status.
3. Examine an existing inbound rule and document its protocol, port, scope and profile.
4. In an isolated VM, create a narrowly scoped temporary test rule if needed.
5. Remove the temporary rule and confirm security posture is restored.

**Verify:** The test rule is removed and expected default firewall profiles remain enabled.

## Lab 04 — Observe BIOS/UEFI behavior
**Objective:** Identify boot mode and boot entries.

1. Inside an authorized test Windows VM, run `msinfo32` and note BIOS Mode.
2. Use `bcdedit /enum` in an elevated command prompt to inspect boot configuration without modifying it.
3. Examine the VM's firmware configuration and boot order.
4. Document the difference between firmware initialization and Windows Boot Manager.

**Verify:** Capture OS boot mode and a description of the boot path.

## Lab 05 — Gather hardware diagnostics (simulation)
**Objective:** Practice incident evidence collection.

1. Pick a lab-generated POST/boot-error scenario or an instructor-provided screenshot.
2. Identify the equipment manufacturer and model, beep code or LED pattern.
3. Check the appropriate vendor reference for that exact hardware revision.
4. Draft a support ticket containing timestamps, symptoms, impact, logs, recent changes and troubleshooting performed.

**Verify:** Another student could reproduce your diagnostic reasoning from the ticket.

## Lab 06 — Maintenance window change plan
**Objective:** Prepare a production-style controlled reboot plan without touching production.

1. Define the affected server and business service.
2. Specify approval, scheduled window, owner, contacts, pre-checks, backups, rollback, reboot procedure and post-validation.
3. Write a sample communication to stakeholders.
4. Simulate the procedure only in a disposable Windows Server VM.
5. Document any failure and a potential RCA format.

**Verify:** The plan has a rollback decision point and named acceptance criteria.
