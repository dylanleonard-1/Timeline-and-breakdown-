# CyberSec Warfare: Offensive + Defensive Vulnerability Automation Lab

**Author:** Dylan Leonard  
**Company:** CyberSec Warfare  
**Mission:** Training the next wave of defenders and automating real-world security.

---

## About Me

I build tools that simulate real threats, automate defense, and teach people how to respond.  
Through my company **CyberSec Warfare**, I’ve developed a complete ecosystem for red + blue team simulation, AI-powered threat detection, and compliance-ready patching systems.

These tools power:
- My personal cybersecurity training systems
- The active defense of clients in healthcare, retail, and fintech
- Live SIEM integrations for threat testing and compliance assurance

---

## CVS Health Alignment

After researching CVS Health’s public security incident in 2021 (1B+ records exposed due to cloud misconfiguration), I chosen from the tools I have to show AI-driven threat simulation and remediation platform to proactively prevent such incidents across:
- OT (Operational Tech)
- IoT (Internet of Things)
- AI/ML Security

---

## My Solutions for CVS Health

### 1. `AutoRed` – MITRE-Aligned Threat Emulation  
Simulates real-world attacks:
- T1566 (Phishing), T1110.001 (SSH Brute), T1190 (SQLi), T1021 (Lateral), T1071 (Beaconing)
- Full telemetry via JSON + Splunk/Sentinel
- Helps test MTTR, SOAR playbooks, and blue team readiness

**→ [View AutoRed Simulation](autored_perfect_final.html)**

---

### 2. `RiskRank-AI` – CVE Prioritization Engine  
- Calculates dynamic risk score from CVSS + EPSS + SLA urgency
- Adds asset context (public, crown-jewel, internal)
- Logs for dashboards / remediation boards

**→ [View RiskRank-AI Logic](riskrank_ai.html)**

---

### 3. `SLAWatchdog` – Patch Enforcement + Escalation  
- Monitors SLA deadlines
- Reads `AutoBlue` patch logs
- Sends breach alerts to Splunk/Sentinel

**→ [View SLA Enforcement](sla_watchdog.html)**

---

### 4. `AutoBlue` – Real Remediation with SIEM Proof  
- Validates patches with SHA256 hashes
- Logs to JSON → Splunk
- Integrates with Qualys / Tenable / Prisma
- Fully CTEM-ready

**→ [View AutoBlue Engine](autoblue.html)**

---

### 5. `WebHound-AI` – Headless JavaScript Threat Scanner  
- AI-style scoring for obfuscated JS, redirect chains, formjackers
- Checks domains via VirusTotal
- Logs verdicts and threats for SOC review

**→ [View WebHound-AI](webhound_ai.html)**

---

## Technology Stack

- **Languages:** Python, Bash, PowerShell
- **Frameworks:** MITRE ATT&CK, NIST 800-53, ISO 27001
- **Tools Used:** Qualys, Tenable, Shodan, Splunk, Sentinel, VirusTotal, Wireshark
- **Security Domains:** OT/IoT/AI Threats, SLA, Patch Compliance, CTEM, Threat Simulation

---

## Strategy for CVS Health

### Proposed Plan (based on 2021 incident):

1. **Audit** cloud/IaC environments for misconfigurations
2. **Use AutoBlue** to validate and log every patch
3. **Scan all IoT/OT/AI assets** using WebHound-AI and Shodan integrations
4. **Continuously test defenses** with AutoRed simulations
5. **Track everything** with SLAWatchdog and RiskRank-AI dashboards

---

## Expandability

All modules are:
- Modular
- Token-authenticated
- Built to integrate with **any SIEM or SOAR**

If CVS Health uses tools I haven’t listed? That’s fine—my engines are designed to adapt.

---

## Want to See It Live?

Ask me for a **demo walkthrough** or deploy the lab using Docker or Python3 on Ubuntu.  
Each module is self-documenting and built for CI/CD security.

---

## Contact

**Dylan Leonard**  
CyberSec Warfare  
GitHub: [@dylanleonard-1](https://github.com/dylanleonard-1)  
LinkedIn: [linkedin.com/in/dylan-leonard-sec](https://linkedin.com/in/dylan-leonard-sec)
