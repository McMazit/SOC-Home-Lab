# Incident 002 — Process Execution Investigation

## Severity

Medium

## Status

Investigated

## Detection

Windows process creation events were collected from CLIENT01 and analyzed in Splunk.

## Data Sources

- Windows Security Event Log
- Event ID 4688
- Splunk Enterprise
- Splunk Universal Forwarder
- Wazuh

## Investigation

Event ID 4688 records process creation activity on Windows systems.

Splunk query:

```spl
index=main host=CLIENT01 EventCode=4688

The investigation focused on identifying:

Process name
Parent process
Executing user
Command-line activity
Timestamp
Related processes
SOC Investigation Workflow
Process Creation
      ↓
Identify Process
      ↓
Identify User
      ↓
Review Parent Process
      ↓
Review Command Line
      ↓
Correlate With Other Events
      ↓
Determine Risk
Response

The activity was investigated within the isolated lab environment.

No production systems were affected.

Lessons Learned
Event ID 4688 provides valuable endpoint process telemetry.
Process activity should be correlated with authentication and PowerShell events.
Parent-child process relationships can help identify suspicious execution chains.
