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
## Security Configuration Assessment (SCA)

Wazuh was used to perform a Security Configuration Assessment against CLIENT01 using the CIS Microsoft Windows 11 Enterprise Benchmark.

The assessment generated security findings related to Windows password and account security configuration.

Examples included:

- Minimum password length
- Minimum password age
- Maximum password age
- Password history enforcement
- Windows security configuration compliance

## Threat Hunting & Event Investigation

Wazuh Threat Hunting was used to investigate security telemetry collected from CLIENT01.

The investigation included:

- Reviewing Windows Security events
- Filtering events by CLIENT01
- Reviewing authentication activity
- Investigating process creation events
- Examining Wazuh rule IDs and severity levels
- Reviewing security configuration findings

The Wazuh dashboard recorded hundreds of events from the monitored endpoint, providing a centralized view for SOC investigation.

## Evidence

Screenshots demonstrating the lab are stored in the `screenshots/` directory.

Evidence includes:

- Wazuh agent connected and active
- Wazuh Threat Hunting dashboard
- CLIENT01 security events
- CIS Windows security configuration findings
- Process creation events
- Wazuh event investigation

## Skills Demonstrated

- Wazuh SIEM/EDR monitoring
- Windows security event analysis
- Security Configuration Assessment
- Threat hunting
- Event filtering and investigation
- Alert and rule analysis
- Endpoint monitoring
- SOC investigation workflow
