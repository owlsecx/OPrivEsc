# 🦉 OPrivEsc

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-OForensics-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-Proprietary-orange?style=flat-square"/>
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

This tool is part of the **OwlSec** suite — a collection of 275+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

Proprietary — © 2026 Owlsec LLC. All rights reserved.

*Tools are distributed as pre-built executables. Source code is proprietary.*

---

## 🔍 Verification & Transparency

This tool is closed-source. These files let you see exactly what is inside it,
without the source:

- [`SBOM.cdx.json`](SBOM.cdx.json) — CycloneDX inventory: SHA-256 of this
  binary, bundled CPython version, and every bundled library with its exact
  version and license. Feed it to Grype, Trivy or Dependency-Track to audit
  our dependencies for CVEs yourself.
- [`THIRD-PARTY-NOTICES.md`](THIRD-PARTY-NOTICES.md) — the full license text
  of every third-party component, extracted from this binary.

**No telemetry, no analytics, no licence check-in.** This tool does not phone
home. Verify that claim yourself:

```bash
sudo strace -f -e trace=network ./OPrivEsc --help   # watch every network call
firejail --net=none ./OPrivEsc --help               # deny the network entirely
```

Release signing, GPL compliance and vulnerability reporting:
[**TRUST.md**](https://github.com/owlsecx/owl-os/blob/main/TRUST.md)
