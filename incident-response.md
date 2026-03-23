# Incident Resposne

## What is Incident Response ?
Structured process of investigating, containing, recovering and learning form security incidents.

## 6 Phases:
1: Preparation - set up tools, write playabooks, train team
2: Identification - confirm if alert is real or false positive
3: Containment - stop damage spreading (isolate device, block IP)
4: Eradication - remove malware, patch vulnerability
5: Recovery - restore from backup, bring systems online
6: Lesson Learned - what happened, how to prevent next time 

## Alert Triage:
Determining if alert is real threat or false positive
- True Postive = real attack -> investigate
- Fase Positive = normal actyivity -> close alert

## 5 Investigative Questions:
- What happened ?
- When did it start ?
- Where did it come from ?
- Who is responsible ?
- How did they do it ?

## Real World Experience:
Mapped real ransomware attack  to IR pahses:
- No preparation beofre attack = massive damage
- After attack: implemented backups, network segmentation, building SOC now