# SOC Home Lab

A hands-on blue-team cybersecurity portfolio lab focused on security monitoring, Windows authentication analysis, SIEM queries, alert triage and incident investigation.

## Goal

Build practical SOC analyst evidence using synthetic and lab-generated telemetry, then document each investigation clearly enough to explain in a technical interview.

## Skills Demonstrated

- Windows Event Log analysis
- SIEM monitoring and investigation
- Microsoft Sentinel KQL
- Splunk SPL
- Alert triage and event correlation
- Incident investigation
- MITRE ATT&CK mapping
- Containment and remediation planning
- Technical security documentation

## Completed Investigation

### Brute-Force Login Investigation ✅
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

➡️ [View the investigation](./investigations/brute-force/)

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
    └── brute-force/
        ├── README.md
        ├── incident_report.md
        ├── sentinel_queries.kql
        ├── splunk_queries.spl
        ├── analysis_summary.json
        ├── sample_authentication_events.csv
        └── PUBLISH_CHECKLIST.md
```

## Current Status

- [x] Project structure created
- [x] Brute-force investigation completed
- [x] Sentinel KQL added
- [x] Splunk SPL added
- [x] Incident report added
- [x] MITRE ATT&CK mapping added
- [ ] Windows VM telemetry project
- [ ] Sysmon investigation
- [ ] PowerShell investigation
- [ ] Network investigation
- [ ] Screenshots from a live SIEM lab

## Portfolio Integrity

The completed brute-force investigation currently uses **synthetic data**. It demonstrates analysis and detection logic and is not presented as commercial SOC experience.

## Author

**Kishore Bandi**  
MSc Cyber Security & Penetration Testing | BTech Computer Science Engineering  
Target roles: Junior SOC Analyst • Cyber Security Analyst • Security Operations • Junior Security Engineer
