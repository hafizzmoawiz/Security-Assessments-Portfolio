# Security Assessment Portfolio

Hands-on security testing work completed during an 8-week **Software Security Testing internship at the National CERT of Pakistan (PKCERT/NCERT)**, covering four domains: web application security, network/infrastructure security, mobile application security, and API security.

Every finding in this repository was independently identified, reproduced, and documented with proof-of-concept evidence and remediation guidance, following a consistent methodology of automated scanning + manual verification.

> **Note:** All testing was performed exclusively against intentionally vulnerable, purpose-built training applications and an isolated lab environment (DVWA, OWASP Juice Shop, Metasploitable2, DIVA, VAmPI) — no real, third-party, or production systems were tested. This repository is for portfolio/educational purposes only.

## Contents

| Domain | Target(s) | Report(s) |
|---|---|---|
| [01 — Web Application Security](./01-web-application-security) | DVWA, OWASP Juice Shop | Recon & automated scanning, manual OWASP Top 10 testing |
| [02 — Network / Infrastructure Security](./02-network-infrastructure-security) | Metasploitable2 | Recon, vulnerability scanning, and exploitation validation |
| [03 — Mobile Application Security](./03-mobile-application-security) | DIVA (Damn Insecure and Vulnerable App) | Static (MobSF/JADX/Apktool) + dynamic (Emulator/Burp/ADB) analysis |
| [04 — API Security](./04-api-security) | VAmPI (Vulnerable API) | Endpoint mapping, manual authorization testing, automated scanning |

## Tools Used

`Nmap` `OpenVAS (Greenbone)` `Metasploit Framework` `Burp Suite` `OWASP ZAP` `Nikto` `WhatWeb` `MobSF` `JADX` `Apktool` `Postman` `Swagger / OpenAPI` `ADB` `SQLite` `Kali Linux`

## Skills Demonstrated

- Reconnaissance and automated vulnerability scanning across web, network, mobile, and API targets
- Manual exploitation and verification of OWASP Top 10 (Web) and OWASP API Security Top 10 issues
- Static and dynamic mobile application analysis, including manifest/Smali-level source review
- Chained, cross-tool evidence verification (e.g. confirming a static-analysis prediction with live runtime data)
- Professional security report writing: executive summaries, severity-rated findings, proof-of-concept evidence, and remediation recommendations

## Summary of Key Findings Across All Domains

| Severity | Approx. Count | Examples |
|---|---|---|
| Critical | 10+ | SQL Injection, Broken Object Level Authorization (BOLA), Mass Assignment, unauthenticated admin/database endpoints, plaintext credential storage |
| High | 12+ | Insecure data storage, known service backdoors, passwordless remote login, default credentials |
| Medium / Low / Informational | 15+ | Missing security headers, verbose logging, weak session/token lifetime, exported components |

*(Exact counts and full detail are in each domain's reports.)*

## About

**Hafiz Muhammad Moawiz** — BS Cybersecurity student, Software Security Testing intern at National CERT of Pakistan (PKCERT).
