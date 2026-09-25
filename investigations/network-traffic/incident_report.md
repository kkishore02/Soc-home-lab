# Incident Report — Suspicious Network Beaconing

## Executive Summary

Synthetic network evidence was reviewed for workstation `10.10.20.15`. The host resolved `update-check.example` to `203.0.113.77` and then initiated repeated HTTP connections to that external destination at approximately one-minute intervals.

The periodic pattern, unusual external destination and repeated check-in URI are consistent with behaviour that would warrant investigation for possible command-and-control activity.

## Scope

**Source host:** `10.10.20.15`  
**Destination IP:** `203.0.113.77`  
**Domain:** `update-check.example`  
**Protocol:** DNS, TCP, HTTP  
**Destination port:** 80

## Timeline

| Time | Activity | Analyst Note |
|---|---|---|
| 06:30:01 | DNS query for `update-check.example` | Suspicious domain lookup |
| 06:30:01 | DNS response returns `203.0.113.77` | External destination identified |
| 06:30:03 | TCP session begins to port 80 | Outbound connection |
| 06:30:04 | HTTP GET to `/checkin?id=wkstn15` | First observed check-in |
| 06:31:04 | Repeated HTTP GET | ~60-second interval |
| 06:32:04 | Repeated HTTP GET | Periodic pattern continues |
| 06:33:04 | Repeated HTTP GET | Beacon-like behaviour |
| 06:34:04 | Repeated HTTP GET | Consistent periodicity |

## Indicators

- Internal host: `10.10.20.15`
- External IP: `203.0.113.77`
- Domain: `update-check.example`
- URI: `/checkin?id=wkstn15`
- Protocol: HTTP
- Port: 80

## Analysis

The sequence begins with a DNS lookup followed almost immediately by an outbound HTTP connection. The same URI is then requested repeatedly at roughly one-minute intervals.

Periodic outbound communication can be associated with legitimate applications, so timing alone is not sufficient to classify the traffic as malicious. However, the combination of an unusual domain, a dedicated external destination and repeated check-in behaviour would justify endpoint correlation and further investigation.

Recommended next steps would include checking the originating process on the workstation, reviewing DNS and proxy history, validating the destination against threat-intelligence sources, and examining whether the same destination was contacted by other hosts.

## MITRE ATT&CK Mapping

- **Tactic:** Command and Control
- **Technique:** Application Layer Protocol: Web Protocols
- **Technique ID:** T1071.001

## Analyst Conclusion

**Classification:** Suspicious — requires escalation and endpoint correlation.

The available synthetic evidence supports a hypothesis of possible beaconing behaviour, but it does not independently prove malware or compromise.

## Recommended Actions

1. Identify the process responsible for the connections.
2. Review endpoint telemetry around the first connection.
3. Search enterprise DNS/proxy logs for the destination.
4. Check whether other hosts contacted the same domain/IP.
5. Block the destination if validated as malicious.
6. Isolate the endpoint if corroborating malicious activity is found.

## Integrity Note

This report uses synthetic evidence for portfolio practice and does not represent a real customer or production incident.
