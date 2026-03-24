# Complete SOC Pipeline - Real World Attack Analysis
## The Complete SOC Architecture

OPNsense (Network Control)
    |
Suricata (Behavioral Detection)
    |
Wazuh SIEM (Log Correaltion and Alerting)
    |
MISP (threat intelligence)
    |
SOAR (Automated Response)
    |
EDR/XDR (Endpoint Monitoring)
    |
SOC Dashboard (Analyst View)

## Every Tool and its Job
Tool   |  Job
OPNsense   | Control Network Traffic
Suricata   | Detect Behavioral Steps
Wazuh      | Correlates logs and Alerts
MISP       | Provides threat intelligence
SOAR       | Automated Response
EDR/XDR    | Monitor Endpoints
IR Process | Structured Investigation
Dashboard  | Visualizes everything


## Real Attack Analysis - Ransomware Incident
01:47am - Port scan detected (Reconnaissance)
01:52am - RDP Brute force attempt (Credential Access)
01:53am - Successful RDP Login (Intial Access)
01:54am - Malware dropped in temp folder (Excecution)
01:55am - C2 connection established (Command and Control)
01:58am - Mass file Encryption (Impact)

### MITRE ATT&CK Mapping:
- T1046 - Network Scanning
- T1110 - Brute Force
- T1078 - Valid Accounts
- T1059 - Command Line Interface
- T1071 - C2 communication
- T1486 - Data encrypted for impact

### SOAR Response
Event 2 - Brute force:
-> Temporarily block Ip
-> Alert analyst

Event 3 - Successful login at 2am:
-> Terminate session immediately
-> Disable adminstrator account
-> Page analyst - CRITICAL!

Event 5 - C2 connection:
-> Isolate device immediately
-> Block outbound connection
-> Take memory snapshot

Event 6 - Mass encryption:
-> Device already isolated
-> Check MISP for decryption key
-> Begin backup restoration

### Incident Response Phase:
1:Preparation - SOC tool configured
2:Identification - confirmed real atttack
3:Contanment - device isolated, Ip blocked
4: Eradication - Malware removed, credential reset
5: Recovery - Restore from backup
6: Lesson Learned - Update playbooks

### IOCs Added to MISP:
- IP: 203.54.231.10 (attacker IP)
- IP: 185.220.101.10 (C2 server)
- File hash: hash of update.exe
- Port: 4444 (C2 port)

### What went wrong?
- No automatic block on brute force
- No alert on login outside office hours
- No outbound connection monitoring
- SOAR playbooks not configured

### Prevention:
- Auto block after 10 failed login
- Alert on login after buisness hours
- Block unknown outbound connection
- Automatic C2 connection via MISP
- File Integrity Monitoring(FIM) on critcal folders
- Regular backups
- Disable RDP from internet - use VPN

## Key Lessons
1: SOAR handles containment - humans handles decison
2: Every attac leaves IOCs - share them via MISP
3: Detection at earlist stage = minimum damage
4: Preparation before attack = everything
5: Logs are your digital forensic evidence





