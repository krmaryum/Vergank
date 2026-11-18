# Vergank — Infrastructure Administration Learning Portfolio

**VMware • Wintel / Windows Server • Microsoft Azure AZ-104**

A practical, bilingual (English + Roman Urdu) learning repository documenting infrastructure-administration classes, lab exercises, technical concepts, interview preparation, and troubleshooting.

> **Learning workflow:** Learn → Understand → Practice → Verify → Document → GitHub

## 📚 Study tracks

| Track | Focus | Browse |
|---|---|---|
| **AZ-104** | Microsoft Azure administration, cloud fundamentals, identity, networking, storage and compute | [AZ-104/](AZ-104/) |
| **VMware** | Virtualization, ESXi, vCenter, Active Directory integration, and infrastructure labs | [VMware/](VMware/) |
| **Wintel** | Windows Server, identity, data center fundamentals and enterprise administration | [Wintel/](Wintel/) |

These links point to the **existing** top-level folders. Detailed lesson files can be added gradually; the table does not imply every planned lab is already complete.

## 🧭 How to use this repository

1. Choose a study track above.
2. Open the relevant class/day folder and read the **English** or **Roman Urdu** notes.
3. Review the summary and interview questions.
4. Work through any available hands-on lab, recording commands and results.
5. Compare your results with the verification checklist and save sanitized screenshots.
6. Record technical corrections separately from the instructor's original explanations.

## 🗂️ Suggested layout for **future** classes

The following layout is a **proposed standard**, not a claim about the current repository. Existing files stay in place until reviewed and deliberately moved.

```text
Vergank/
├── README.md
├── AZ-104/
│   ├── Day-01/
│   └── Day-02/
├── VMware/
│   └── Day-01-ADDS/
└── Wintel/
    └── Day-01/
```

Inside a future day folder:

```text
Day-XX-Topic/
├── README.md
├── English/
├── Roman_Urdu/
├── Summary_Reports/
├── Interview_QA/
├── Hands_On_Labs/
├── Technical_Verification/
└── Screenshots/
```

**Recommended file names:** `Day-02_Detailed_English.md`, `Day-02_Detailed_Roman_Urdu.md`, `Day-02_Summary_English.md`, and `Day-02_Interview_QA_English.md`.

## 📝 Documentation principles

- Preserve the full instructor explanation and classroom examples in detailed notes; do not silently shorten into a summary.
- Keep **English** and **Roman Urdu** versions separately navigable.
- Put shorter revision summaries in `Summary_Reports`.
- Separate **source-based lecture content** from additional explanations and technical corrections.
- Give labs: **Objective → Prerequisites → Steps → Verification → Troubleshooting → Cleanup**.
- Include realistic interview questions and scenario-based exercises whenever useful.
- Do not commit passwords, API keys, access tokens, unredacted private IP inventories, company/client data, or sensitive screenshots.
- Avoid committing VM disks (`.vmdk`, `.vhdx`), ISO images, installers, and other large binaries.

## 🎯 Current learning priorities

- **Azure AZ-104:** cloud and on-premises models, IaaS/PaaS/SaaS, cost models, cloud resource management.
- **VMware:** ESXi/vCenter foundations, identity integration, lab validation, operational troubleshooting.
- **Wintel:** Windows Server, AD DS, DNS, DHCP, enterprise server builds and data center planning.

These are areas of study, not certifications or project-completion claims.

## 🔗 Reference documentation

- [Microsoft Learn — Azure](https://learn.microsoft.com/azure/)
- [Microsoft Learn — Windows Server](https://learn.microsoft.com/windows-server/)
- [VMware documentation](https://docs.vmware.com/)
- [GitHub Markdown documentation](https://docs.github.com/en/get-started/writing-on-github)

## ⚠️ Notes and attribution

This is a personal educational project. Class notes may include instructor-derived explanations. Technical correction notes distinguish verified guidance from classroom statements. Product names belong to their respective owners; this repository is not an official Microsoft, VMware, or Broadcom publication.

---

*Maintained as an evolving hands-on learning record.*
