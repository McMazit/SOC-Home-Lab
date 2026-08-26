# SOC Home Lab

Hands-on cybersecurity home lab simulating a small enterprise SOC environment.

## Overview

This project combines Active Directory, Windows endpoints, Wazuh, Splunk Enterprise, and Kali Linux to simulate security monitoring, detection, investigation, and incident response.

## Lab Architecture

```text
                    Kali Linux
                        │
                   Attack Simulation
                        │
                        ▼
              ┌──────────────────┐
              │    CLIENT01      │
              │ Windows Endpoint │
              └────────┬─────────┘
                       │
                       │
              ┌────────▼─────────┐
              │      DC01        │
              │ Active Directory │
              └──────────────────┘

CLIENT01
   │
   ├── Wazuh Agent ──────► Wazuh Manager
   │                           │
   │                           ▼
   │                    Wazuh Dashboard
   │
   └── Splunk Universal Forwarder
                               │
                               ▼
                         Splunk Enterprise
Technologies
Splunk Enterprise
Splunk Universal Forwarder
Wazuh
Windows Server / Active Directory
Windows endpoint monitoring
Kali Linux
VMware Workstation
PowerShell
Windows Security Event Logs
Projects
1. Active Directory Security Lab

Built a Windows domain environment with:

Domain Controller
Windows client
Domain users
Authentication monitoring
Windows Security Event Logs
2. Wazuh Detection Lab

Configured Wazuh to monitor Windows endpoint activity.

Implemented custom detection for PowerShell/process execution.

Example detection:

Rule ID: 100100
Severity: 10
User: Alice
Process: powershell.exe
Event: Windows Event ID 4688
3. Splunk SIEM Lab

Configured:

Splunk Enterprise
Splunk Universal Forwarder
TCP receiving on port 9997
Windows Security Event Collection

Investigated:

Event ID 4624 — Successful Logon
Event ID 4625 — Failed Logon
Event ID 4688 — Process Creation
SOC Investigation Workflow
Alert
  ↓
Validate
  ↓
Identify User / Host / IP
  ↓
Analyze Event
  ↓
Correlate Related Events
  ↓
Determine Scope
  ↓
Assess Threat
  ↓
Contain / Escalate
  ↓
Document Incident
Skills Demonstrated
SIEM monitoring
Windows event analysis
Authentication investigation
Process monitoring
Detection engineering
PowerShell monitoring
Active Directory security
Log collection
Incident investigation
Basic incident response
