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


Commit it.

### After that

We'll create the **main portfolio README improvements**, then finish the repository structure. **Screenshots come last.**
done
Step 12 — Create the Lab Architecture documentation

Create:

05-Architecture/README.md

Paste:

# SOC Lab Architecture

## Overview

This lab simulates a small enterprise SOC environment using isolated virtual machines.

## Infrastructure

| System | Role |
|---|---|
| Kali Linux | Attack simulation |
| DC01 | Active Directory Domain Controller |
| CLIENT01 | Windows endpoint |
| Wazuh | Endpoint monitoring and detection |
| SplunkVM | SIEM and log analysis |

## Data Flow

```text
                    KALI
                     │
              Attack Simulation
                     │
                     ▼
              ┌─────────────┐
              │  CLIENT01   │
              │  Windows 11 │
              └──────┬──────┘
                     │
              ┌──────┴──────┐
              │             │
              ▼             ▼
           Wazuh          Splunk
           Agent          Forwarder
              │             │
              ▼             ▼
       Wazuh Manager   Splunk Enterprise
              │             │
              └──────┬──────┘
                     ▼
                 SOC Analyst
Network

The lab machines operate on an isolated VMware virtual network.

Security Monitoring

The environment provides visibility into:

Authentication
Process execution
PowerShell activity
Windows Security Events
Endpoint security events
Active Directory activity
SOC Workflow
Attack Simulation
       ↓
Endpoint Activity
       ↓
Log Collection
       ↓
SIEM / Detection Platform
       ↓
Alert
       ↓
SOC Investigation
       ↓
Incident Response
Objective

The goal of the lab is to develop practical SOC analyst skills through controlled attack simulation, security monitoring, detection, investigation, and incident response.
