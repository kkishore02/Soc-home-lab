# SOC Home Lab Setup

## Environment

Recommended minimum setup:

- Windows 11 virtual machine
- Sysmon
- Wazuh or Splunk
- VirtualBox, VMware or another hypervisor
- Host-only or NAT networking for the lab

## Step 1 — Prepare the Windows VM

1. Create a Windows 11 virtual machine.
2. Apply Windows updates.
3. Create a local test user.
4. Take a clean snapshot before generating test activity.

## Step 2 — Install Sysmon

Install Microsoft Sysmon and use a reputable community configuration appropriate for a defensive lab.

Confirm that Sysmon events appear in:

`Applications and Services Logs > Microsoft > Windows > Sysmon > Operational`

Important event types to become familiar with include:

- Process creation
- Network connections
- File creation
- Registry activity
- DNS queries

## Step 3 — Install the SIEM

Choose either Wazuh or Splunk for the first version of the project.

For an entry-level SOC portfolio, the goal is not just installation. The important evidence is showing that you can:

- ingest Windows logs,
- search them,
- identify suspicious patterns,
- explain an alert,
- document an investigation.

## Step 4 — Connect the Endpoint

Forward Windows/Sysmon telemetry to the SIEM and verify that events from the Windows VM are searchable.

## Step 5 — Build Detection Scenarios

Start with simple defensive scenarios:

1. Repeated failed logins
2. Suspicious PowerShell execution
3. Unusual process creation
4. New local-user creation
5. Network connection investigation

## Step 6 — Document Everything

For every scenario, add:

- the detection objective,
- logs used,
- query,
- alert screenshot,
- investigation steps,
- MITRE ATT&CK mapping,
- conclusion,
- remediation.
