# SOAR - Security Operations Automation Response
## What is SOAR?
Automatically responds to security alerts without waiting for human intervention.

## 3 Components
- Orchestration: Connects all security tools together
- Automation: Removes human from repititive tasks
- Response: Takes action when threat is detected

## What is a Playbook ?
Predefined response workflow:
"When THIS happens - do THESE steps automatically"

## Types of Response:
- Automated: Happens without human
- Semi-automated: SOAR suggests, human approves
- Manual: Human decides everything

## Key Rule:
SOAR handles containment - human handles decisons!

## How SOAR connects to other tools:
Wazuh alert -> SOAR triggered -> MISP checked -> Firewall updated -> Ticket created -> Analyst notified

## Real world Example:
Ransomware detected ->
Device isolated automatically ->
MISP checked for decrytion key ->
Analyst paged for backup decison