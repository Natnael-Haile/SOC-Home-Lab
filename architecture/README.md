# Wazuh SOC Home Lab — Architecture

## Overview

Designed and deployed a virtualized Security Operations Center (SOC) lab using Microsoft Hyper-V and Wazuh SIEM to practice security monitoring, threat detection, and incident investigation.

## Infrastructure

| Machine | Role | Host Address |
|---|---|---|
| Hyper-V Host | Virtual network interface | .1 |
| WIN-01 | Windows endpoint with Sysmon and Wazuh Agent | .10 |
| SIEM-01 | Wazuh Manager and Dashboard | .20 |
| KALI-01 | Security testing environment | .30 |

All three virtual machines operate within a dedicated isolated SOC lab network.

## Completed Configuration

- Provisioned WIN-01, SIEM-01, and KALI-01 using Microsoft Hyper-V.
- Configured a dedicated virtual network for controlled security testing.
- Installed Sysmon on WIN-01 to collect detailed Windows endpoint telemetry.
- Configured Wazuh to collect the Sysmon event channel.
- Deployed the Wazuh Manager and Dashboard on SIEM-01.
- Installed and connected the WIN-01 Wazuh agent.
- Verified that the Windows endpoint agent is active.

## Security Monitoring Workflow

1. WIN-01 generates Windows and Sysmon security telemetry.
2. The Wazuh Agent collects configured event channels.
3. Events are forwarded to the Wazuh Manager on SIEM-01.
4. Wazuh processes events using its detection rules.
5. Analysts review security events and alerts through the Wazuh Dashboard.

## Current Phase

**Phase 5 — Detection Testing**

The next objective is to generate controlled activity in the lab, verify that Wazuh receives the relevant telemetry, and determine whether detection rules produce the expected alerts.

## Planned Investigations

- Failed authentication attempts
- PowerShell execution activity
- Network scanning
- Suspicious file and process behavior

## Next Deliverables

- Architecture diagram
- Wazuh alert screenshots
- Investigation case studies
- MITRE ATT&CK mappings
- Final SOC incident report
