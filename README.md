# CyberSec Warfare: Offensive + Defensive Vulnerability Automation Lab

**Author:** Dylan Leonard  
**Company:** CyberSec Warfare  
**Mission:** Training the next wave of defenders and automating real-world security.

---

## About Me

I build tools that simulate real threats, automate defense, and teach people how to respond.  
Through my company **CyberSec Warfare**, I’ve developed a full-cycle ecosystem for red + blue team simulation, AI-powered threat detection, and compliance-ready patching systems.

These tools support:
- Personal cybersecurity training environments
- Real client defenses across healthcare, fintech, and retail
- Continuous SIEM/SOAR-based validation and threat simulation

---

## CVS Health Alignment

After analyzing CVS Health’s public misconfiguration breach in 2021 (1B+ session/device records exposed), I identified multiple ways to proactively prevent such threats across:
- OT (Operational Technology)
- IoT (Internet of Things)
- AI/ML Security

I mapped my existing tools into a complete CTEM (Continuous Threat Exposure Management) solution designed for real-time visibility, SLA enforcement, and remediation at scale.

---

## CyberSec Warfare Platform Architecture (Enterprise-Integrated Diagram)

```
                          [ Executive Dashboard / Compliance / CISO ]
                                          ▲
                                          │
                                          ▼
                           ┌─────────────────────────────┐
                           │  Splunk / Microsoft Sentinel│
                           └─────┬───────────────────────┘
                                 │  Receives logs + alerts
                                 ▼
      ┌────────────┬────────────┴────────────┬────────────┐
      ▼            ▼                         ▼            ▼
[RiskRank-AI]  [SLAWatchdog]           [AutoBlue]   [WebHound-AI]
  ▲                ▲                      ▲             ▲
  │                │                      │             │
  │     ┌──────────┴───────────┐   ┌──────┴────────┐    │
  │     │     CVSS / EPSS      │   │ Patch Validation │  │
  │     │  Asset Criticality   │   │ SHA256, Timestamp│  │
  │     └──────────┬───────────┘   └─────────────────┘  │
  │                │                                    │
  ▼                ▼                                    ▼
[Prioritized CVEs] ────────────────┐        [Browser Threats: JS, C2, Redirects]
                                   ▼
                             ┌────────────┐
                             │ AutoRed    │
                             └────┬───────┘
                                  ▼
               [Red Team TTPs: Phishing, SQLi, Lateral, Beaconing]
                                  ▼
                             JSON logs (MITRE aligned)

                ◄────────────────────[ FEEDS BACK ]────────────────────►
                        To SIEM dashboards, SOAR playbooks, alerts

──────────────────────────── External Data Sources ────────────────────────────

[Employee Devices / Workstations]       [IoT/OT Devices: HVAC, Sensors, RFID]
        │                                         │
        ▼                                         ▼
┌────────────────────┐                  ┌────────────────────────────┐
│     CVE Scanning   │◄─Input──────────▶│ Protocol Scanning (Zigbee, │
│ (Tenable / Qualys) │                  │ MQTT, CoAP, Bluetooth)     │
└────────────────────┘                  └────────────────────────────┘
        │                                         │
        ▼                                         ▼
[Device Risk Feed]                         [Firmware + API Vulnerability Scan]
        │                                         │
        └───────► Sent to CTEM Pipeline ──────────┘

```

**Legend:**
- Arrows show telemetry flow and threat injection/detection feedback loops
- External devices (employees, OT/IoT) contribute vulnerabilities or are test targets
- Splunk/Sentinel receive ALL output: telemetry, alerts, CVE reports, and breach simulations
- All tools modular and ready for compliance use (HIPAA, PCI-DSS, ISO 27001, NIST 800-53)


## Tool Breakdown

### 1. `AutoRed` – MITRE-Adversary Simulation  
- T1566 (Phish), T1110.001 (SSH), T1190 (SQLi), T1021 (Lateral), T1071 (C2)
- Simulates active threats + logs real telemetry to Splunk/Sentinel
- Measures MTTR, alert response, and blue team visibility

**→ [View AutoRed Simulation](autored_perfect_final.html)**

---

### 2. `RiskRank-AI` – Dynamic CVE Risk Prioritization  
- Combines CVSS, EPSS, asset criticality, and SLA logic
- Generates ranked CVE list with tags + remediation timelines

**→ [View RiskRank-AI](riskrank_ai.html)**

---

### 3. `SLAWatchdog` – SLA Enforcement & Escalation  
- Monitors unpatched CVEs
- Escalates breached SLA targets to Splunk/Sentinel
- Interfaces directly with AutoBlue patch logs

**→ [View SLA Watchdog](sla_watchdog.html)**

---

### 4. `AutoBlue` – Patch Automation with Proof  
- Validates patches with pre/post SHA256 hashes
- Creates compliance-grade JSON reports
- Integrates with Tenable, Qualys, Prisma

**→ [View AutoBlue Engine](autoblue.html)**

---

### 5. `WebHound-AI` – JavaScript Threat Hunter  
- Uses Selenium + custom AI pattern scoring
- Identifies malicious JS (eval, base64, beacons, etc.)
- Checks external scripts via VirusTotal & URLScan

**→ [View WebHound-AI](webhound_ai.html)**

---

## Stack & Skills

- **Languages:** Python, Bash, PowerShell
- **Security Frameworks:** MITRE ATT&CK, NIST 800-53, ISO 27001, PCI-DSS
- **Tools:** Qualys, Tenable, Wiz, Prisma, VirusTotal, Shodan, Wireshark
- **Integrations:** Splunk (HEC), Microsoft Sentinel, SOAR pipelines
- **Domains:** OT/IoT/AI Security, Red Team Simulation, Patch Enforcement, CTEM

---

## CVS Strategy Overview

### Incident Response:
- Validate patching via AutoBlue
- Escalate SLA violations with SLAWatchdog
- Simulate real attackers with AutoRed

### IoT/OT Security:
- Scan Zigbee/MQTT/CoAP firmware configs
- Identify vulnerable embedded systems
- Shodan + WebHound-AI for exposed interfaces

### AI/ML Security:
- Detect poisoning/inversion risks
- Perform model integrity checks

---

## Deployment & Modularity

All tools are:
- Self-contained Python modules
- Built with REST API forwarding support
- Designed to plug into **any SIEM or SOAR**

Tokens, paths, and modules are modular for enterprise adoption.

---

## Demo & Contact

Ask for a live **walkthrough**, full PDF export, or dashboard tour.  
This suite is built for real SOC use, training, and compliance auditing.

**Author:** Dylan Leonard  
**GitHub:** [@dylanleonard-1](https://github.com/dylanleonard-1)  
**LinkedIn:** [linkedin.com/in/dylan-leonard-sec](https://linkedin.com/in/dylan-leonard-sec)
