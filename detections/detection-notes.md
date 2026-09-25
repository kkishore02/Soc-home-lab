# Detection Notes

Use this file to record detection logic as the lab develops.

## Failed Login Detection

**Objective:** identify repeated authentication failures from the same source or against the same account.

**Useful telemetry:** Windows authentication events.

**Questions to investigate:**
- How many failures occurred?
- Were they followed by a successful login?
- Were multiple accounts targeted?
- Was the source expected?
- Did suspicious activity occur after authentication?

## Suspicious PowerShell Detection

**Objective:** identify PowerShell activity that warrants analyst review.

**Useful telemetry:**
- Process creation
- Parent process
- Command line
- PowerShell logging

**Questions to investigate:**
- Which user launched PowerShell?
- What was the parent process?
- What command was executed?
- Was the command expected for that host/user?
- Were network connections or child processes created?
