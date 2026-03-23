# EDR?XDR

## What is EDR ?
Endpoint Detection and Response
Monitors everything inside the individual devices:
- Process monitoring (what programs are running)
- File system monitoring (files created/modified/deleted)
- Registry monitoring (Windows setting changes)
- Network connections from device
- User behavior

## What is XDR ?
Extended Detection and Response
EDR + Multiple Other sources combined:
- Endpoints (EDR)
- Network (OPNsense)
- Threat intel
- Cloud logs 
- Email monitoring

##  Simple diffrence
- EDR = security camera inside one room 
- XDR = security cameras everywhere connected together

## How Wazuh implement EDR/XDR ?
- Wazuh Agent = EDR (monitors individual device)
- Wazuh Manager + Multiple sources = XDR

## FIM (File Integrity Monitoring)
Monitors critical files and folders
Any unexpected change = immediate alert
Critical for detecting ransomware early 

## Real World
Phishing email -> cmd.exe launched by outlook.exe
-> Malware dropped in temp folder
-> C2 connection established
-> EDR cathces it before done !

