# Incident 003 — Suspicious PowerShell Activity

## Severity

High

## Status

Planned Investigation

## Objective

Investigate suspicious PowerShell execution on CLIENT01 and determine whether the activity represents malicious behavior.

## Data Sources

- Windows Security Event Logs
- PowerShell logs
- Event ID 4688
- Wazuh
- Splunk

## Investigation

The investigation will focus on:

- PowerShell process execution
- Executing user
- Parent process
- Command-line arguments
- Script activity
- Network connections
- Related authentication events

## Investigation Workflow

```text
PowerShell Execution
        ↓
Identify User
        ↓
Identify Parent Process
        ↓
Analyze Command Line
        ↓
Review PowerShell Events
        ↓
Correlate Authentication
        ↓
Check Network Activity
        ↓
Determine Malicious Intent
        ↓
Contain / Escalate
Splunk Investigation

Example search:

index=main host=CLIENT01 EventCode=4688
Response

Any suspicious PowerShell activity would be investigated, validated, and escalated according to severity.

Lessons Learned

PowerShell telemetry provides valuable visibility into attacker activity and should be correlated with process creation, authentication, and network events.
