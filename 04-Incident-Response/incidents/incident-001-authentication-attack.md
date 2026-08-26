# Incident 001 — Failed Authentication

## Severity

Medium

## Status

Investigated

## Detection

A Windows failed authentication event (Event ID 4625) was detected on CLIENT01.

## Affected Host

CLIENT01

## Data Sources

- Windows Security Event Log
- Splunk Enterprise
- Splunk Universal Forwarder
- Wazuh

## Event

Windows Event ID 4625 indicates that an account failed to log on.

## Investigation

The event was generated in the isolated SOC lab and successfully forwarded from CLIENT01 to Splunk.

Splunk query:

```spl
index=main host=CLIENT01 EventCode=4625
The event was reviewed to determine:

Authentication timestamp
Target account
Logon type
Source information
Failure reason
Related authentication activity
Timeline
Failed authentication attempt generated on CLIENT01.
Windows Security generated Event ID 4625.
Splunk Universal Forwarder collected the event.
Event was forwarded to Splunk Enterprise.
SOC investigation identified the event.
Event was classified as a controlled lab simulation.
Response

No production systems were affected.

The event was generated intentionally as part of the SOC detection and investigation exercise.

Lessons Learned
Windows Event ID 4625 is useful for detecting failed authentication.
Authentication events should be correlated with successful logons.
SIEM visibility is essential for investigating account-related activity.
