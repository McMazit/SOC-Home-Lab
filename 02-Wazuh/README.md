# Wazuh Detection & Monitoring Lab

## Objective

Configured Wazuh to monitor a Windows endpoint and analyze security telemetry for SOC detection and investigation.

## Environment

- Wazuh Manager
- Wazuh Dashboard
- CLIENT01 Windows endpoint
- Wazuh Agent
- Windows Event Logs

## Activities

- Installed and configured the Wazuh agent
- Connected CLIENT01 to the Wazuh manager
- Monitored Windows security events
- Investigated authentication activity
- Monitored process execution
- Created and tested security detections
- Investigated alerts through the Wazuh dashboard

## Detection Focus

The lab focused on detecting suspicious Windows activity including:

- Authentication failures
- Successful authentication
- PowerShell execution
- Process creation
- Suspicious command execution

## SOC Workflow

```text
Windows Endpoint
       ↓
Wazuh Agent
       ↓
Wazuh Manager
       ↓
Security Alert
       ↓
Investigation
       ↓
Determine Severity
       ↓
Response / Escalation
