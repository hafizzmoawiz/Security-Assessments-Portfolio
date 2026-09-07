# Mobile Application Security

Static and dynamic security analysis of **DIVA (Damn Insecure and Vulnerable App)**, an intentionally vulnerable Android application, on an Android Emulator.

## Reports

| Report | Focus | Tools |
|---|---|---|
| [Week 5 — Static Analysis Report](./Week5-Static-Analysis-Report.pdf) | Automated + manual static analysis: decompilation, permissions, hardcoded secrets, insecure storage | MobSF, JADX, Apktool |
| [Week 6 — Dynamic Analysis Report](./Week6-Dynamic-Analysis-Report.pdf) | Runtime analysis: network traffic interception, live storage/logging inspection, access-control testing | Android Emulator, Burp Suite, ADB |

## Key Findings

- **Access Control Bypass** — two independent unprotected app components exposed vendor API credentials with no authentication (confirmed via Android intent analysis and live testing)
- **SQL Injection** — a single crafted input disclosed all user records, including a credit card number
- **Insecure Data Storage** — credentials and PINs stored in plain text across three separate mechanisms (external file, SharedPreferences, SQLite database), confirmed live via ADB
- Debuggable production build, dangerous permissions, and an exported content provider

Several dynamic (Week 6) findings directly confirmed, with live runtime evidence, predictions first made from static source-code analysis in Week 5 — demonstrating a complete static-to-dynamic verification chain.

## Skills Demonstrated

- APK decompilation and manifest/Smali-level source code review
- Automated (MobSF) and manual (JADX/Apktool) static analysis, cross-verifying every automated finding
- Dynamic testing: emulator setup, proxy/certificate configuration for HTTPS interception, and ADB-based runtime storage inspection
- Correctly identifying when an automated tool's finding needed reclassification after manual verification (avoiding false-positive reporting)
