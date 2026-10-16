# 🦉 OSnmpdX

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Linux-0a0c10?style=flat-square"/>
  <img src="https://img.shields.io/badge/Category-ONetwork-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Part%20of-OwlSec%20Toolkit-7b5ea7?style=flat-square"/>
  <img src="https://img.shields.io/badge/Version-1.0.0-cyan?style=flat-square"/>
</p>

> **OSnmpdX** — Net-SNMP Agent Configuration Auditor

---

> ⚠️ **AUTHORISED USE ONLY** — Use only on systems you own or have explicit written permission to test. Unauthorised use is illegal.

---

## 📌 Overview

Net-SNMP snmpd / snmptrapd / snmp.conf configuration security auditor

---

## ✨ Features

- Offline, read-only parsers for snmpd.conf, snmpd.local.conf (+ includeFile / includeDir), /var/lib/snmp persistent USM store, snmptrapd.conf and snmp.conf client defaults
- Community checks — default / weak strings, any rwcommunity, missing source, com2sec 'default'
- SNMPv3 checks — noauth / authNoPriv, MD5 / DES, short / reused / example passphrases, rwuser
- VACM view exposure — full tree, hrSWRun process args, ARP table, EXTEND-MIB write → RCE
- Handler checks — extend / exec / pass / traphandle world-writable, relative, /tmp, run as root
- AgentX / SMUX / proxy / listener exposure
- Service args (-u / -g / -D / -Lf) & systemd units
- Persistent-dir permissions, EOL version notes
- CWE + MITRE ATT&CK mapping, severity, remediation
- Score + grade, hardened templates, self-test demo
- Export TXT / MD / JSON / CSV / SARIF 2.1.0
- Secrets (communities, passphrases, keys) masked

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage

```bash
./OSnmpdX
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
