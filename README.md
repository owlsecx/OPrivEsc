# 🦉 OPrivEsc

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OPrivEsc** — Local Privilege Escalation Enumerator

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

OPrivEsc is a local privilege-escalation enumerator for Linux. It reads local configuration — SUID/SGID binaries, sudo rights, writable sensitive paths, cron and systemd timers, processes and mounts — and reports findings with a score. It never attempts escalation, runs no exploits and makes no system changes.

---

## ✨ Features

- System enumeration with kernel/OS version, offline CVE hints and PATH analysis
- SUID/SGID inventory cross-referenced against a GTFOBins-like dataset plus capabilities
- Sudo rights analysis (sudo -l / sudoers) for NOPASSWD and abusable binaries
- Writable sensitive files, cron jobs and systemd timers detection
- Credentials hunt (locations only, values masked) and root-process/socket review
- NFS/mount checks, scoring and TXT/MD/JSON/CSV reporting with a CI fail-on gate

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPrivEsc --all
./OPrivEsc --suid --sudo --cron
./OPrivEsc --all --format json -o report.json
./OPrivEsc --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
