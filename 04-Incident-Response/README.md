# Incident Response Lab

## Objective

Simulate SOC incidents and practice the complete security investigation and incident response lifecycle using Splunk and Wazuh.

## Investigation Lifecycle

```text
Alert
  ↓
Triage
  ↓
Evidence Collection
  ↓
Investigation
  ↓
Scope Determination
  ↓
Containment
  ↓
Remediation
  ↓
Recovery
  ↓
Lessons Learned
Planned Investigations
Incident 001 — Authentication Attack

Investigate suspicious failed authentication activity on CLIENT01.

Data sources:

Windows Security Events
Splunk
Wazuh

Relevant Event ID:

4625 — Failed Logon
4624 — Successful Logon
Incident 002 — Suspicious Process Execution

Investigate suspicious process execution on CLIENT01.

Data sources:

Windows Event ID 4688
Splunk
Wazuh
Incident 003 — PowerShell Activity

Investigate suspicious PowerShell execution and determine whether the activity is malicious.

SOC Analyst Investigation

For each incident, the investigation will identify:

Source IP
Affected host
Username
Timestamp
Process/activity
Related events
Attack technique
Severity
Scope
Recommended response
Skills Demonstrated
Alert triage
Log analysis
Event correlation
Timeline reconstruction
Threat investigation
Incident classification
Containment planning
Incident documentation
