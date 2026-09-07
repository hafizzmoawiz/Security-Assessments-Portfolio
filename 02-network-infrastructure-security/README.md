# Network / Infrastructure Security

Network reconnaissance, automated vulnerability scanning, and manual exploitation validation against **Metasploitable2**, an intentionally vulnerable Linux host, in an isolated lab network.

## Reports

| Report | Focus | Tools |
|---|---|---|
| [Week 3-4 — Full Network Assessment Report](./Week3-4-Full-Network-Assessment-Report.pdf) | **Consolidated final report:** host discovery, port/service scanning, automated vulnerability scanning, and manual exploitation validation with proof-of-concept evidence | Nmap, OpenVAS (Greenbone), Metasploit Framework, netcat |
| [Week 3 — Recon and Scanning (standalone)](./Week3-Recon-and-Scanning-standalone.pdf) | Original standalone recon/scanning report (superseded by the combined Week 3-4 report above) | Nmap, OpenVAS |

## Key Findings

Out of 116 automated findings, the following Critical-severity issues were manually validated and exploited to confirm real, working access:

- **vsftpd 2.3.4 backdoor** — remote root shell via Metasploit
- **Ingreslock backdoor (port 1524)** — direct, unauthenticated root shell via netcat
- **rlogin passwordless login** — direct root access with no credentials
- **MySQL/MariaDB default credentials** — full database access with a blank root password
- DistCC RCE — attempted (not successful in this test run, documented as a negative result)

## Skills Demonstrated

- Host discovery, port/service enumeration, and OS fingerprinting with Nmap
- Automated vulnerability scanning and CVSS-based severity triage with OpenVAS
- Manual exploitation and proof-of-concept validation using Metasploit and manual tools
- Distinguishing confirmed, exploitable findings from theoretical automated-scan output
