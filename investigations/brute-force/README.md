# SOC Brute-Force Investigation

Personal SOC lab demonstrating investigation of a simulated RDP brute-force attack using synthetic Windows authentication logs.

## Key Findings
- **155 failed logons** from one source IP against `admin`
- Followed by successful Event ID **4624**
- Followed by privileged Event ID **4672**
- Logon Type **10**
- Mapped to **MITRE ATT&CK T1110 / T1078**

## Skills
Windows event analysis • SOC triage • Sentinel KQL • Splunk SPL • event correlation • MITRE ATT&CK • incident reporting • containment planning

## Files
- `synthetic_windows_authentication_logs.csv`
- `sentinel_queries.kql`
- `splunk_queries.spl`
- `incident_report.md`
- `analysis_summary.json`
- `failed_logons_timeline.png`

## Integrity
This repository is a **personal lab using synthetic data**.
