# SOC Lab Setup Progress

## Date: March 31, 2026

## What i built Today:
- Installed Wazuh SIEM on Ubuntu VM (VirtualBox)
- Configured Wazuh Manager, Indexer and Dashboard
- Connected Windows laptop as Wazuh agent
- Verified real security alerts in dashboard

## Lab Architecture
- Wazuh Server: Ubuntu VM -> 192.168.29.74
- Agent: Windows laptop (Arpit-laptop)
- Dashboard: https://192.168.29.74

## Real Alerts Seen:
- T0178 Valid Accounts (login events)
- T1562.001 Impair Defenses (agent stopped)
- Authentication success/failure events

## Next Step:
- Set up Kali Linux VM
- Simulate real attacks
- See detection in Wazuh
