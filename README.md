# Cybersecurity Internship — Maincrafts Technology

**Intern:** Benidict David

Lab-based cybersecurity internship work — building intentionally vulnerable environments and assessing them with industry-standard tooling.

---

## Task 2 — Lab Build

**Date:** 27 June 2026

Built a personal cybersecurity lab using Oracle VirtualBox + Kali Linux + OWASP Juice Shop (Docker). Tools validated: Nmap, Wireshark, Burp Suite.

**File:** [`Task-2/Benidict_David_Task2_Lab_Report.pdf`](./Task-2/Benidict_David_Task2_Lab_Report.pdf)

**Tools:** Oracle VirtualBox 7.x · Kali Linux 2026.1 · OWASP Juice Shop (Docker) · Nmap 7.99 · Wireshark · Burp Suite Community Edition

**Network:** NAT adapter for internet access (10.0.2.0/24) · Host-Only adapter for isolated lab traffic (192.168.56.0/24)

---

## Task 3 — Vulnerability Scanning & Assessment

**Date:** 7 July 2026

Performed a vulnerability assessment against Metasploitable2 (192.168.56.103) and OWASP Juice Shop (Docker, port 3000), using Nmap, Nikto, and Dirsearch for host discovery, port/service enumeration, and web-layer scanning. Identification and documentation only — no exploitation, per task scope.

**File:** [`Task-3/VAR_Task3_Benidict.pdf`](./Task-3/VAR_Task3_Benidict.pdf)

**Tools:** Nmap 7.99 · Nikto v2.6.0 · Dirsearch v0.4.3

**Key findings:**
- Metasploitable2 — backdoored vsftpd 2.3.4 (CVE-2011-2523) and UnrealIRCd (CVE-2010-2075), default Tomcat Manager credentials, cleartext r-services (rsh/rlogin/rexec)
- Juice Shop — wildcard CORS policy, missing HSTS/CSP headers, no rate limiting (directory brute-forcing at default thread count reproducibly degraded the service)

Full risk ratings, impact analysis, and remediation are in the PDF.
<<<<<<< HEAD

---

## Task 4 — Exploitation & Web Application Security Testing

**Date:** 18 July 2026

Conducted web application penetration testing against local instances of Damn Vulnerable Web App (DVWA) and OWASP Juice Shop. Successfully identified and exploited critical web vulnerabilities, configured intercepting proxies, and performed automated directory enumeration.

**File:** [`Maincrafts_PenTest_Report task 4.pdf`](./Maincrafts_PenTest_Report%20task%204.pdf)

**Tools:** Burp Suite Community Edition · Firefox (FoxyProxy) · Dirsearch

**Key findings:**
- **DVWA** — SQL Injection (Critical) allowing database dumping via tautology payloads (`1' OR '1'='1' #`).
- **DVWA** — Reflected Cross-Site Scripting (High) demonstrating arbitrary JavaScript execution in the browser.
- **Juice Shop** — Information Disclosure via Hidden Directories (Medium) discovered via automated brute-forcing with Dirsearch.

Full methodology, screenshots, risk assessments, and remediation strategies (Parameterized Queries, Output Encoding) are in the PDF.
=======
>>>>>>> 9a5958f3507fc42a6f28c482345749fef3e26d10
"# cybersecurity-internship" 
