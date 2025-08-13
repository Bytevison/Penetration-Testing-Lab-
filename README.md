# Security Operations & Assurance – Penetration Testing & Vulnerability Assessment (Lab)

This project was completed as part of my postgraduate studies in **Security Operations & Assurance**.  
It demonstrates a full **penetration testing and vulnerability assessment** workflow in a **safe, isolated lab environment**.

> ⚠️ **Ethics Notice:** All testing was performed with explicit permission in a controlled lab using intentionally vulnerable systems (Metasploitable-2, DVWA, WebGoat).  
> No production systems were harmed.

---

## 📋 Overview

The project covered:
- Host discovery and service enumeration
- Vulnerability scanning and prioritisation
- Web application security testing
- Exploitation of a selected vulnerability
- Remediation planning and security hardening

---

## 🛠️ Lab Setup

**Operating Systems / Targets**
- Kali Linux (attacker)
- Metasploitable-2 (vulnerable Linux server)
- DVWA (Damn Vulnerable Web Application)
- WebGoat (OWASP insecure Java web app)

**Tools**
- `Nmap` – Host discovery, port scanning, service enumeration
- `OpenVAS` – Vulnerability scanning and severity scoring
- `OWASP ZAP` – Web application scanning (SQLi, XSS, insecure headers)
- `Metasploit Framework` – Exploit demonstration and post-exploitation
- `Wireshark` – Network traffic analysis (spot checks)

---

## 🔍 Methodology

1. **Network Discovery**
   - Used Nmap to identify live hosts and open ports in the lab.
   - Performed service and version enumeration.

2. **Vulnerability Scanning**
   - Scanned identified hosts with OpenVAS.
   - Categorised vulnerabilities into **High**, **Medium**, **Low** severity.

3. **Web Application Testing**
   - Used OWASP ZAP to test DVWA and WebGoat for:
     - SQL Injection
     - Missing CSP and anti-CSRF tokens
     - Insecure cookies
   - Captured evidence and reproduced issues.

4. **Exploitation**
   - Selected a high-severity vulnerability.
   - Executed the exploit using Metasploit.
   - Validated impact and gathered post-exploitation evidence.

5. **Remediation**
   - Recommended security controls:
     - Patch management
     - TLS hardening
     - Secure coding practices (e.g., parameterised queries)
     - Least privilege and network segmentation

---

## 📊 Key Findings

| Severity | Example Finding                                    | Tool         |
|----------|----------------------------------------------------|--------------|
| High     | Outdated Apache Tomcat vulnerable to RCE           | OpenVAS      |
| High     | Weak SSH/TLS cipher suites                         | OpenVAS/Nmap |
| Medium   | SQL Injection in login form                        | ZAP          |
| Medium   | Missing Content Security Policy headers            | ZAP          |
| Low      | Insecure session cookies                           | ZAP          |

---

## 🚀 Results

- Mapped the complete attack surface for the lab environment.
- Successfully exploited a high-risk vulnerability to demonstrate real-world impact.
- Provided a prioritised remediation plan based on risk and feasibility.

---


