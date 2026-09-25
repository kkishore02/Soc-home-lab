# SOC Investigation Template

## Incident Title

Example: Multiple Failed Logins Followed by Successful Authentication

## Detection Objective

Describe what behaviour the detection is intended to identify.

## Data Sources

- Windows Event Logs
- Sysmon
- SIEM alerts

## Relevant Event IDs

List the Event IDs used in the investigation.

## Timeline

| Time | Event | Host/User | Analyst Notes |
|---|---|---|---|
| | | | |

## Indicators

Record relevant:

- usernames
- source IPs
- destination IPs
- process names
- command lines
- hashes
- domains

## SIEM Query

```text
Add the query/search used here.
```

## Investigation

Explain what happened, how the events relate to one another and what evidence supports the conclusion.

## MITRE ATT&CK Mapping

- Tactic:
- Technique:
- Technique ID:

## Analyst Conclusion

State whether the activity appears benign, suspicious or malicious, and explain why.

## Recommended Actions

- Contain affected account/host if required
- Reset credentials if appropriate
- Block malicious indicators
- Review related authentication/activity
- Improve detection coverage
