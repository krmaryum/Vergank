# Wintel Lab

**Language:** English | [Roman Urdu](README.roman-urdu.md)

Beginner-friendly, step-by-step study bundles for my **Wintel (Windows on Intel) class lab**: installing Windows Server and Windows as virtual machines in **VMware Workstation Pro** on a Windows 10 host.

Every bundle has the same parts, in **English and Roman Urdu**:

- **README**: the full install guide, one screenshot per step, with a simple "Why?" for each step.
- **TROUBLESHOOTING**: real problems and fixes (Symptom, Cause, Fix, Lesson).
- **INTERVIEW-QA**: 25 beginner interview questions and answers.
- **quiz.html**: a 25-question practice quiz. Download it and open it in any browser; it works offline.

## Bundles

| Bundle | Status | Guide | Troubleshooting | Interview Q&A | Quiz |
|--------|--------|-------|-----------------|---------------|------|
| **Windows Server 2019** | ✅ Done | [English](WS2019/README.md) · [Roman Urdu](WS2019/README.roman-urdu.md) | [English](WS2019/TROUBLESHOOTING.md) · [Roman Urdu](WS2019/TROUBLESHOOTING.roman-urdu.md) | [English](WS2019/INTERVIEW-QA.md) · [Roman Urdu](WS2019/INTERVIEW-QA.roman-urdu.md) | [quiz.html](WS2019/quiz.html) |
| Windows Server 2022 | 🔜 Coming | | | | |
| Windows Server 2025 | 🔜 Coming | | | | |
| Windows 11 | 🔜 Coming | | | | |

## Where to start

New to virtual machines? Start with **[Windows Server 2019](WS2019/README.md)**. It explains every term from the beginning.

## Lab environment

- Host: Windows 10 Pro, Intel i5-4430 (4 cores), 16 GB RAM
- Hypervisor: VMware Workstation Pro 25H2
- VMs stored on `D:\VMs`

## Repository layout

```
wintel-lab/
├── README.md               (this page)
├── README.roman-urdu.md
├── WS2019/                 (done)
│   ├── README.md / README.roman-urdu.md
│   ├── TROUBLESHOOTING.md / TROUBLESHOOTING.roman-urdu.md
│   ├── INTERVIEW-QA.md / INTERVIEW-QA.roman-urdu.md
│   ├── quiz.html
│   └── images/
├── WS2022/                 (coming)
├── WS2025/                 (coming)
└── Win11/                  (coming)
```

**Note:** No passwords or product keys are stored in this repository. Never commit your own.
