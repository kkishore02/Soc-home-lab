# Wireshark Network Traffic Investigation

A hands-on SOC portfolio investigation using **synthetic network traffic evidence** to demonstrate packet-analysis, protocol triage and suspicious-connection investigation with Wireshark-style workflows.

## Scenario

A workstation is suspected of contacting an unusual external host shortly after a user opens a suspicious attachment. The objective is to review network evidence, identify suspicious patterns, extract indicators and document an analyst conclusion.

## Key Findings

- Repeated outbound connections from one internal workstation to an unusual external IP
- DNS lookup for a suspicious domain immediately before the outbound connection
- HTTP traffic to a non-standard destination
- Repeated beacon-like connections at short intervals
- Internal host communicating with a destination not observed elsewhere in the sample
- Activity mapped to MITRE ATT&CK command-and-control concepts

## Skills Demonstrated

- Wireshark packet-analysis workflow
- TCP/IP and DNS analysis
- HTTP traffic triage
- Display-filter construction
- IOC extraction
- Timeline correlation
- Network-based threat hunting
- MITRE ATT&CK mapping
- SOC incident reporting

## Files

- `synthetic_network_traffic.csv` — synthetic packet/event evidence
- `wireshark_display_filters.txt` — useful Wireshark display filters
- `incident_report.md` — SOC-style investigation report
- `iocs.json` — extracted indicators
- `analysis_summary.json` — concise investigation summary

## Example Wireshark Workflow

1. Identify the suspected endpoint.
2. Filter traffic to/from the endpoint.
3. Review DNS queries.
4. Inspect unusual destination IPs and ports.
5. Follow suspicious TCP/HTTP conversations.
6. Compare packet timing for periodic behaviour.
7. Extract domains, IPs and URIs as IOCs.
8. Document the evidence and analyst conclusion.

## MITRE ATT&CK

- **TA0011 — Command and Control**
- **T1071.001 — Web Protocols**

## Portfolio Integrity

This investigation uses **synthetic data** created for portfolio practice. It demonstrates analysis technique and documentation skill and is not presented as commercial SOC experience.
