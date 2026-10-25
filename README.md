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


OSnmpdX is an offline, read-only Net-SNMP agent configuration auditor for snmpd.conf, the USM user store, snmptrapd.conf and snmp.conf. It checks community strings, SNMPv3 users, VACM views, extend/exec RCE handlers and AgentX exposure, masking every secret it encounters. Findings are mapped to CWE and MITRE ATT&CK, scored and graded, and exportable as TXT, Markdown, JSON, CSV or SARIF.

---

## ✨ Features


- Read-only parsers for snmpd.conf, snmpd.local.conf (include file/dir), /var/lib/snmp USM store, snmptrapd.conf and snmp.conf
- Community checks: default/weak strings, any rwcommunity, missing source, com2sec 'default'
- SNMPv3 checks: noauth/authNoPriv, MD5/DES, short/reused/example passphrases, rwuser
- VACM view exposure (full tree, process args, ARP table) and EXTEND-MIB write-to-RCE detection
- Handler checks for extend/exec/pass/traphandle that are world-writable, relative, in /tmp or run as root
- CWE+ATT&CK mapping, score/grade, hardened templates and TXT/MD/JSON/CSV/SARIF export with secrets masked

---

## ⚙️ Requirements

- **Linux**
- **No Python installation needed** — runs as a standalone executable

---

## 🚀 Usage


```bash
./OSnmpdX --scan --format sarif -o snmpd.sarif
./OSnmpdX --snmpd /etc/snmp/snmpd.conf --trapd /etc/snmp/snmptrapd.conf
./OSnmpdX --root /mnt/image --fail-on high
./OSnmpdX --demo
./OSnmpdX --help
```

---

## 📦 Part of OwlSec Toolkit

This tool is part of the **OwlSec** suite — a collection of 300+ security and privacy tools.

🔗 [owlsec.org](https://owlsec.org)

---

## ©️ License

MIT License — © Khaled S. Haddad

*Tools are distributed as pre-built executables. Source code is proprietary.*
