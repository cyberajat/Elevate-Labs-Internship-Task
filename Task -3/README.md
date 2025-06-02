# Elevate Labs Task- 5
Target: Metasploitable2 Machine (IP: 192.168.x.x)
Tool: Nessus Essentials
Scan Type: Basic Network Scan
Scan Duration: ~3 hours
Total Vulnerabilities Found: 57

🔴 Critical: 9

🔺 High: 5

🟡 Medium: 23

🔵 Low: 7

ℹ️ Info: 119

# Critical Vulnerabilities (Top 4)
## 1. Canonical Ubuntu Linux 8.04 (End of Life)
CVE: Not specified, but OS is unsupported.

Security: 🔴 Critical (CVSS 10.0)

Description: OS is no longer receiving security patches, exposing it to many known vulnerabilities.

Fix: Upgrade to a supported version of Ubuntu (e.g., Ubuntu 22.04+).

## 2. VNC Server Uses 'password' as Default
Plugin ID: 61708

Security: 🔴 Critical (CVSS 10.0)

Description: Nessus was able to login using VNC with username: none, password: password.

Impact: Unauthenticated attackers can gain full access to the desktop remotely.

Fix: Set a strong, complex password on VNC service.

## 3. Bind Shell Backdoor Detected
Plugin ID: 51988

Severity: 🔴 Critical (CVSS 9.8)

Description: A shell is accessible over a TCP port with no authentication.

Impact: Full remote control of the system by attackers.

Fix: Investigate the host, remove backdoor, and reinstall OS if needed.

## 4. Apache Tomcat RCE (Remote Code Execution)
Security: 🔴 Critical (CVSS 9.8)

Description: Apache Tomcat server running outdated version allows remote code execution via crafted requests.

## Fix: Upgrade Apache Tomcat to the latest secure version.

⚠️ Medium Risk Example
SSL DROWN Attack Vulnerability
Plugin ID: 89058

Security: 🟡 Medium

Description: SSLv2 is enabled, allowing an attacker to decrypt TLS traffic under certain conditions.

Fix: Disable SSLv2, remove weak cipher suites, and update SSL/TLS libraries.


🧰 Tools Used
Nessus Essentials (https://www.tenable.com/products/nessus/nessus-essentials)

Metasploitable2 as vulnerable test VM
