# SOC Incident Report — Brute-Force Login Investigation

**Project type:** Personal cybersecurity lab using synthetic Windows authentication logs  
**Analyst:** Kishore Bandi

## Executive Summary
Synthetic Windows authentication telemetry showed **155 failed remote logons** from `185.220.101.45` targeting the `admin` account on `SRV-RDP-01`. The burst was followed by a successful Event ID 4624 and then Event ID 4672 (special privileges assigned), which raises the simulated incident from failed brute-force activity to suspected account compromise.

## Evidence
- Source IP: `185.220.101.45`
- Target: `admin` on `SRV-RDP-01`
- Failed logons: **155**
- Successful logon: Event ID **4624**
- Privileged logon: Event ID **4672**
- Logon type: **10 (RemoteInteractive / RDP in this lab scenario)**

## Assessment
**Classification:** Brute-force attack with suspected valid-account compromise  
**Severity:** High  
**Confidence:** High within the synthetic dataset

## MITRE ATT&CK
- **T1110 — Brute Force**
- **T1078 — Valid Accounts**

## Investigation
1. Filtered failed and successful authentication events.
2. Grouped failures by source IP/account and identified the high-volume outlier.
3. Correlated the failure burst with a successful login from the same source/account.
4. Verified the remote interactive logon type.
5. Identified Event ID 4672 immediately after the successful login, indicating privileged context.
6. Raised incident severity and documented containment actions.

## Recommended Response
- Temporarily disable or lock the affected administrator account.
- Revoke active sessions and reset credentials.
- Enforce MFA for remote administrative access.
- Restrict RDP to approved VPN/network paths.
- Block the suspicious source where appropriate.
- Review EDR, PowerShell, process and network telemetry after the successful login.
- Hunt for the same source/account activity across other systems.

## Scope / Integrity
This is a **personal lab using synthetic data** and is not represented as commercial SOC employment.
