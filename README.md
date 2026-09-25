# SOC & Cybersecurity Portfolio Lab

A hands-on cybersecurity portfolio focused on security monitoring, Windows authentication analysis, phishing triage, network investigation, SIEM queries, incident response and cyber risk/GRC.

## Portfolio Highlights

| Project | Focus | Tools / Skills | Status |
|---|---|---|---|
| Brute-Force Login Investigation | Authentication attack triage | Windows Events, Sentinel KQL, Splunk SPL, MITRE ATT&CK | ✅ Complete |
| Phishing Email Investigation | Email security / IOC analysis | SPF, DKIM, DMARC, Sentinel, Splunk, MITRE ATT&CK | ✅ Complete |
| Wireshark Network Investigation | DNS / TCP / HTTP analysis | Wireshark filters, IOC extraction, traffic correlation | ✅ Complete |
| Cloud HR SaaS Risk Assessment | Cyber Risk / GRC | Risk register, ISO 27001 concepts, NIST CSF, DPIA, supplier assurance | ✅ Complete |

**Recruiter quick view:** This portfolio demonstrates hands-on blue-team analysis, SIEM query writing, incident reporting, network investigation and cyber-risk documentation using clearly labelled synthetic or fictional scenarios.

## Goal

Build practical, explainable portfolio evidence using synthetic and lab-generated data, with clear documentation that can be discussed in technical interviews.

## Skills Demonstrated

- Windows Event Log analysis
- SIEM monitoring and investigation
- Microsoft Sentinel KQL
- Splunk SPL
- Alert triage and event correlation
- Phishing email triage
- IOC extraction
- SPF / DKIM / DMARC interpretation
- Wireshark and network traffic analysis
- Incident investigation
- MITRE ATT&CK mapping
- Containment and remediation planning
- NIST / ISO 27001-aligned risk assessment
- Third-party security assurance
- Privacy / DPIA screening
- Technical security documentation

## Completed Investigations

### 1. Brute-Force Login Investigation ✅
Investigated a simulated RDP brute-force sequence using synthetic Windows authentication logs.

**Key evidence**
- 155 failed Event ID 4625 logons against an administrator account
- Successful Event ID 4624 from the same source
- Event ID 4672 immediately afterwards, indicating privileged context
- Logon Type 10 (RemoteInteractive)
- MITRE ATT&CK: T1110 Brute Force and T1078 Valid Accounts

➡️ [View the brute-force investigation](./investigations/brute-force/)

### 2. Phishing Email Investigation ✅
Investigated a synthetic Microsoft 365 credential-phishing email.

**Key evidence**
- Lookalike sender domain
- From / Reply-To mismatch
- SPF and DMARC failures
- No DKIM signature
- Suspicious credential-reset URL
- MITRE ATT&CK: T1566.002 and T1056.003

➡️ [View the phishing investigation](./investigations/phishing-email/)

### 3. Wireshark Network Traffic Investigation ✅
Investigated synthetic DNS, TCP and HTTP traffic to identify suspicious periodic outbound communication.

**Key evidence**
- Suspicious DNS lookup from an internal workstation
- External destination contacted over HTTP
- Repeated check-ins at approximately 60-second intervals
- IOC extraction for host, domain, IP and URI
- Wireshark display filters documented
- MITRE ATT&CK: TA0011 Command and Control and T1071.001 Web Protocols

➡️ [View the network traffic investigation](./investigations/network-traffic/)

## Cyber Risk & GRC Project

### Cloud HR SaaS Risk Assessment ✅
Assessed a fictional UK organisation's adoption of a cloud HR SaaS platform.

**Coverage**
- Privileged MFA and access-control gaps
- Third-party / supplier assurance
- Cloud configuration risk
- Vulnerability management
- Incident response responsibilities
- Business continuity
- UK GDPR / DPIA screening
- NIST CSF and ISO 27001-aligned control concepts

**Artifacts**
- Risk register
- Control-gap analysis
- Supplier security assessment
- Privacy / DPIA screening
- Executive summary
- Residual-risk and remediation ownership

➡️ [View the GRC assessment](./grc/cloud-hr-saas-risk-assessment/)

## Planned Lab Scenarios

### Suspicious PowerShell Activity
Monitor process creation and command-line activity for suspicious PowerShell usage.

### Sysmon Process Investigation
Analyse Sysmon process-creation events and unusual parent/child relationships.

### Live SIEM Evidence
Add screenshots and evidence from a configured SIEM environment to complement the synthetic investigations.

## Repository Structure

```text
cybersecurity-portfolio/
├── README.md
├── docs/
├── detections/
├── queries/
├── investigations/
│   ├── brute-force/
│   ├── phishing-email/
│   └── network-traffic/
└── grc/
    └── cloud-hr-saas-risk-assessment/
```

## Current Status

- [x] Brute-force investigation
- [x] Phishing email investigation
- [x] Wireshark network traffic investigation
- [x] Microsoft Sentinel KQL
- [x] Splunk SPL
- [x] MITRE ATT&CK mapping
- [x] Cyber Risk & GRC assessment
- [ ] Windows VM telemetry project
- [ ] Sysmon investigation
- [ ] PowerShell investigation
- [ ] Screenshots from a live SIEM lab

## Portfolio Integrity

The lab investigations and GRC scenario use **synthetic or fictional data**. They demonstrate practical analysis, documentation and security reasoning and are not presented as commercial SOC, penetration-testing or GRC consulting experience.

## Author

**Kishore Bandi**  
MSc Cyber Security & Penetration Testing | BTech Computer Science Engineering  
Target roles: Junior SOC Analyst • Cyber Security Analyst • Security Operations • Junior Security Engineer • Vulnerability Management • Cyber Risk / GRC
