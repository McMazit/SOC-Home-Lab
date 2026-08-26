# Splunk SIEM Lab

## Objective

Deployed Splunk Enterprise as a centralized SIEM and integrated CLIENT01 using the Splunk Universal Forwarder to collect and investigate Windows security telemetry.

## Environment

- Splunk Enterprise
- Splunk Universal Forwarder
- CLIENT01 Windows endpoint
- Windows Security Event Logs
- TCP 9997 receiving port

## Configuration

The Splunk Universal Forwarder was configured on CLIENT01 to send Windows event data to the Splunk Enterprise server.

Data flow:

```text
CLIENT01
   ↓
Splunk Universal Forwarder
   ↓
TCP 9997
   ↓
Splunk Enterprise
   ↓
Search & Investigation
Log Sources

Collected Windows telemetry included:

Windows Security Events
Application Events
System Events
Process Creation Events
Security Investigations
Successful Logon — Event ID 4624
index=main host=CLIENT01 EventCode=4624

Used to investigate successful authentication activity.

Failed Logon — Event ID 4625
index=main host=CLIENT01 EventCode=4625

Used to identify failed authentication attempts.

Process Creation — Event ID 4688
index=main host=CLIENT01 EventCode=4688

Used to investigate process execution on the Windows endpoint.

Security Event Investigation
index=main host=CLIENT01 sourcetype=WinEventLog:Security

Used to investigate Windows Security telemetry.

Detection Testing

A controlled failed authentication attempt was generated on CLIENT01, producing Windows Event ID 4625.

The event was successfully forwarded through the Universal Forwarder and detected in Splunk.

Evidence

Screenshots demonstrating:

Splunk event ingestion
Windows Security events
Successful authentication events
Process creation events
Splunk search and investigation
Skills Demonstrated
Splunk Enterprise
SPL
SIEM deployment
Log ingestion
Windows event analysis
Authentication investigation
Process monitoring
Detection testing
Security event correlation
SOC investigation
