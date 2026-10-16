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

Local privilege-escalation enumerator (audit only — LinPEAS-style)

---

## ✨ Features

- System info — kernel + offline CVE version-range hints, OS release, sudo version notes, PATH analysis
- SUID/SGID inventory with embedded GTFOBins-like cross-reference (~80 binaries) + getcap capabilities
- Sudo rights — sudo -l (timeout) / sudoers parse; NOPASSWD, abusable binaries, env_keep
- Writable sensitive files — passwd/shadow/crontab/ systemd/init/PATH dirs; world-writable service paths
- Cron & systemd timers — writable script detection
- Credentials hunt — locations only, values masked
- Processes & sockets — root procs with writable bins
- NFS/mounts — no_root_squash, fstab nosuid, docker
- Score + report TXT/MD/JSON/CSV; save chooser; clipboard; interactive menu; ~/OPrivEsc/config.json
- Full CLI — --all --suid --sudo --cron --creds --writable --json -o --fail-on --version --help

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OPrivEsc
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
