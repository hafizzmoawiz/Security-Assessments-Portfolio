# API Security

Endpoint mapping, manual authorization testing, and automated scanning of **VAmPI (Vulnerable API)**, a REST API documented via an OpenAPI (Swagger) specification.

## Report

| Report | Focus | Tools |
|---|---|---|
| [Week 7 — API Security Assessment Report](./Week7-API-Security-Assessment-Report.pdf) | Full API endpoint mapping, authentication flow testing, manual authorization testing, and automated scanning | Postman, Swagger/OpenAPI, OWASP ZAP |

## Key Findings

- **Broken Object Level Authorization (BOLA)** — a standard user's own token was used to retrieve another user's private data (OWASP API Security Top 10 #1)
- **Mass Assignment** — a self-registered account was able to grant itself administrator privileges by adding an undocumented field to the registration request
- **Excessive Data Exposure** — an endpoint returned every user's password in plain text
- **Unauthenticated destructive endpoint** — a database-reset function required no authentication at all
- Missing security headers and an extremely short JWT token lifetime, identified via automated scanning

## Skills Demonstrated

- Mapping a complete API attack surface directly from an OpenAPI/Swagger specification
- Manual, account-to-account authorization testing (BOLA) — a class of vulnerability automated scanners routinely miss
- Configuring an automated scanner (ZAP) to test authenticated traffic via a proxy chain, and recognising the limits of automated scanning alone
- Producing an impact analysis that connects multiple findings together (e.g. self-escalated admin + admin-only endpoint) rather than reporting them in isolation
