# SOC Home Lab

A hands-on blue-team cybersecurity lab for practising security monitoring, log analysis, threat detection and incident investigation.

## Goal

Build a small SOC environment that demonstrates practical analyst skills using Windows telemetry, Sysmon and a SIEM platform such as Wazuh or Splunk.

## Planned Architecture

```text
Windows 11 VM
    |
    v
Sysmon + Windows Event Logs
    |
    v
Wazuh / Splunk
    |
    v
Detection Rules & Alerts
    |
    v
Investigation
    |
    v
MITRE ATT&CK Mapping
```

## Skills Demonstrated

- Windows Event Log analysis
- Sysmon telemetry
- SIEM monitoring
- Alert triage
- Detection engineering
- Threat hunting
- Incident investigation
- MITRE ATT&CK mapping
- Security documentation

## Lab Scenarios

### 1. Failed Login Detection
Detect repeated failed logins and investigate the source.

### 2. Suspicious PowerShell Activity
Monitor PowerShell process creation and command-line activity.

### 3. New Process Execution
Analyse Sysmon process creation events and identify unusual parent/child relationships.

### 4. Brute-Force Behaviour
Identify repeated authentication failures followed by a successful login.

### 5. Network Investigation
Review suspicious connections and correlate activity with endpoint telemetry.

## Evidence to Capture

For every scenario, document:

1. What activity was generated
2. Which logs captured it
3. Relevant Event IDs
4. SIEM query/search used
5. Screenshot of the alert or event
6. Investigation notes
7. MITRE ATT&CK technique
8. Analyst conclusion
9. Recommended remediation

## Repository Structure

```text
soc-home-lab/
├── README.md
├── docs/
│   ├── lab-setup.md
│   └── investigation-template.md
├── detections/
│   └── detection-notes.md
├── screenshots/
└── queries/
    └── queries.md
```

## Current Status

- [x] Project structure created
- [ ] Windows VM prepared
- [ ] Sysmon installed
- [ ] SIEM installed/configured
- [ ] Endpoint connected to SIEM
- [ ] Failed-login scenario completed
- [ ] PowerShell scenario completed
- [ ] Investigation reports added
- [ ] Screenshots added

## Author

**Kishore Bandi**  
Cybersecurity MSc Graduate | Aspiring SOC Analyst
