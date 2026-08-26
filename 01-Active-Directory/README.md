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

![Wazuh Dashboard](screenshots/wazuh-dashboard.png)
