# Web Application Security

Reconnaissance, automated scanning, and manual penetration testing against two intentionally vulnerable web applications: **DVWA** and **OWASP Juice Shop**.

## Reports

| Report | Focus | Tools |
|---|---|---|
| [Week 1 — Recon and Automated Scanning](./Week1-Recon-and-Automated-Scanning.pdf) | Reconnaissance, technology fingerprinting, and automated vulnerability scanning | OWASP ZAP, Nikto, WhatWeb, Wappalyzer |
| [Week 2 — Manual Testing (OWASP Top 10)](./Week2-Manual-Testing-OWASP-Top10.pdf) | Manual exploitation of OWASP Top 10 vulnerability classes | Burp Suite, manual testing techniques |

## Key Findings

- SQL Injection (authentication bypass)
- Cross-Site Scripting (XSS) — including a working session-cookie theft proof-of-concept
- Cross-Site Request Forgery (CSRF) — tested and confirmed protected on sensitive endpoints
- Broken Authentication — weak passwords accepted, no rate limiting
- Security Misconfiguration — publicly exposed directory containing sensitive files
- Missing security headers (CSP)

## Skills Demonstrated

- Automated scanning workflow (ZAP, Nikto, WhatWeb) and result triage
- Manual, hands-on exploitation of classic web vulnerabilities with proof-of-concept evidence
- Risk assessment and remediation recommendations aligned with the OWASP Top 10
