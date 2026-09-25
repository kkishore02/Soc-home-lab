# SOC Home Lab

A hands-on blue-team cybersecurity portfolio lab focused on security monitoring, Windows authentication analysis, phishing triage, SIEM queries, alert triage and incident investigation.

## Goal

Build practical SOC analyst evidence using synthetic and lab-generated telemetry, then document each investigation clearly enough to explain in a technical interview.

## Skills Demonstrated

- Windows Event Log analysis
- SIEM monitoring and investigation
- Microsoft Sentinel KQL
- Splunk SPL
- Alert triage and event correlation
- Phishing email triage
- IOC extraction
- SPF / DKIM / DMARC interpretation
- Incident investigation
- MITRE ATT&CK mapping
- Containment and remediation planning
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

**Artifacts**
- Sentinel KQL detection queries
- Splunk SPL searches
- SOC incident report
- Analysis summary
- Sample authentication evidence

➡️ [View the brute-force investigation](./investigations/brute-force/)

### 2. Phishing Email Investigation ✅
Investigated a synthetic Microsoft 365 credential-phishing email.

**Key evidence**
- Lookalike sender domain
- From / Reply-To mismatch
- SPF failure
- DMARC failure
- No DKIM signature
- Suspicious credential-reset URL
- Urgency and account-suspension pressure
- MITRE ATT&CK: T1566.002 and T1056.003

**Artifacts**
- Phishing indicator table
- IOC file
- Sentinel hunting queries
- Splunk hunting searches
- Full SOC-style incident report
- Synthetic email sample

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

**Artifacts**
- Synthetic network traffic evidence
- Wireshark display filters
- IOC JSON
- Analysis summary
- Full SOC-style incident report

➡️ [View the network traffic investigation](./investigations/network-traffic/)

## Planned Lab Scenarios

### Suspicious PowerShell Activity
Monitor process creation and command-line activity for suspicious PowerShell usage.

### New Process Execution
Analyse Sysmon process-creation events and unusual parent/child relationships.

### Network Investigation
Review suspicious connections and correlate endpoint and network telemetry.

## Repository Structure

```text
soc-home-lab/
├── README.md
├── docs/
├── detections/
├── queries/
└── investigations/
    ├── brute-force/
    ├── phishing-email/
    └── network-traffic/
```

## Current Status

- [x] Project structure created
- [x] Brute-force investigation completed
- [x] Phishing email investigation completed
- [x] Wireshark network traffic investigation completed
- [x] Sentinel KQL added
- [x] Splunk SPL added
- [x] Incident reports added
- [x] MITRE ATT&CK mapping added
- [ ] Windows VM telemetry project
- [ ] Sysmon investigation
- [ ] PowerShell investigation
- [x] Network investigation
- [ ] Screenshots from a live SIEM lab

## Portfolio Integrity

The completed investigations currently use **synthetic data**. They demonstrate analysis and detection logic and are not presented as commercial SOC experience.

## Author

**Kishore Bandi**  
MSc Cyber Security & Penetration Testing | BTech Computer Science Engineering  
Target roles: Junior SOC Analyst • Cyber Security Analyst • Security Operations • Junior Security Engineer
