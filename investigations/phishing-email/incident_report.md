# Phishing Email Investigation Report

**Project type:** Personal cybersecurity lab using a synthetic phishing email  
**Analyst:** Kishore Bandi

## Executive Summary
A synthetic email claiming to be from "Microsoft Security" was investigated after it attempted to pressure a user into following a password-reset link.

The message displayed multiple high-confidence phishing indicators:
- lookalike sender domain using `micros0ft` instead of `microsoft`;
- mismatch between `From` and `Reply-To`;
- SPF failure;
- DMARC failure;
- no DKIM signature;
- high-pressure language;
- credential-reset link hosted on a non-Microsoft domain.

The email was classified as **phishing / credential harvesting**.

## Evidence
- Sender: `security-update@micros0ft-support.example`
- Reply-To: `reset-team@account-verification.example`
- SPF: **fail**
- DKIM: **none**
- DMARC: **fail**
- Synthetic source IP: `203.0.113.77`
- Suspicious URL: `https://login-microsoft365-security.example/reset`

## Social Engineering Indicators
- "URGENT" subject
- Threat of mailbox suspension
- 30-minute deadline
- Password-expiration theme
- Account-verification request

## Classification
**Category:** Credential phishing  
**Severity:** High  
**Confidence:** High within the synthetic lab

## MITRE ATT&CK
- **T1566.002 — Phishing: Spearphishing Link**
- **T1056.003 — Input Capture: Web Portal Capture**

## Recommended Response
1. Quarantine/remove the email from affected mailboxes.
2. Block the sender domain and phishing URL/domain where appropriate.
3. Search for messages with the same sender, subject, URL, or related infrastructure.
4. Check whether any recipient clicked the link.
5. If credentials were entered, reset the password, revoke sessions/tokens, verify MFA, and review sign-in logs.
6. Notify affected users.
7. Preserve the email and headers for investigation.

## Scope / Integrity
This is a **personal lab using a synthetic phishing email**. It is not presented as commercial SOC employment.
