# Phishing Email Investigation

A hands-on SOC portfolio project demonstrating triage of a simulated credential-phishing email using synthetic data.

## Scenario
An employee receives an urgent Microsoft 365 password-expiration email. The message is investigated to determine whether it is legitimate or malicious.

## Key Findings
- Lookalike sender domain: `micros0ft-support.example`
- From / Reply-To mismatch
- SPF: fail
- DKIM: none
- DMARC: fail
- Suspicious non-Microsoft password-reset URL
- Urgency and account-suspension pressure

## Classification
**Credential phishing — High severity**

## Skills Demonstrated
- Email-header analysis
- SPF / DKIM / DMARC interpretation
- IOC extraction
- Social-engineering analysis
- MITRE ATT&CK mapping
- Incident-response recommendations
- SOC-style reporting

## Repository Contents
- `synthetic_phishing_email.eml`
- `phishing_indicators.csv`
- `iocs.json`
- `incident_report.md`
- `sentinel_hunting_queries.kql`
- `splunk_hunting_queries.spl`

## MITRE ATT&CK
- **T1566.002 — Spearphishing Link**
- **T1056.003 — Web Portal Capture**

## Portfolio Integrity
This repository is a **personal lab using synthetic data**. It demonstrates practical investigation skills without claiming commercial SOC experience.
