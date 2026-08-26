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
