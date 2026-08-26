# Active Directory Security Lab

## Objective

Built a Windows Active Directory environment to simulate a small enterprise domain and practice authentication monitoring and security investigation.

## Environment

- DC01 — Windows Domain Controller
- CLIENT01 — Windows client
- Active Directory Domain Services
- Windows Security Event Logs
- PowerShell

## Activities

- Configured a Windows domain environment
- Joined CLIENT01 to the domain
- Created and used domain accounts
- Monitored Windows authentication events
- Investigated successful and failed authentication
- Generated security events for SIEM analysis

## Security Events

| Event ID | Description |
|---|---|
| 4624 | Successful logon |
| 4625 | Failed logon |
| 4688 | Process creation |
| 4720 | User account created |
| 4728 | User added to security-enabled global group |
| 7045 | Service installed |

## SOC Relevance

This environment provides the foundation for detecting:

- Brute-force attacks
- Account compromise
- Privilege escalation
- Suspicious process execution
- Lateral movement
- Persistence

## Evidence

Screenshots and investigation evidence are stored in the project repository.

## Wazuh Integration

Wazuh was deployed to monitor the Windows Active Directory environment and collect security telemetry from CLIENT01.

### Monitoring

- Windows Security Events
- Authentication activity
- Endpoint security events
- File and system activity
- Security alerts

### Evidence

Secreenshots Files
## Splunk SIEM Integration

Splunk was integrated into the Active Directory lab to centralize and investigate Windows security telemetry collected from CLIENT01.

### Monitoring & Investigation

- Windows Security Event Logs
- Successful authentication events (Event ID 4624)
- Process creation events (Event ID 4688)
- Windows endpoint activity
- Authentication and security activity
- Event correlation and investigation using SPL

### Splunk Investigation

Windows Event Logs from CLIENT01 were ingested into Splunk and queried using SPL to investigate authentication and process activity.

Example queries:

```spl
index=main host=CLIENT01 EventCode=4624
index=main host=CLIENT01 EventCode=4688
index=main host=CLIENT01 sourcetype=WinEventLog:Security
Evidence

The repository contains screenshots demonstrating:

Successful authentication events
Windows Security Event 4624
Process creation Event 4688
Security event ingestion into Splunk
Splunk event investigation and filtering
