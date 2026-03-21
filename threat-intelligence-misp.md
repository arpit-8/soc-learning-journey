# Threat Intelligence and MISP

# What is threat intelligence?
Knowledege about known threats, malicious IPs, domains, and malware collected globally.

#What is MISP?
Open source platform where organizations share threat intelligence with each other.

# # KEy Concepts
- IOCs (Indicator of Compromise) - evidence of attack
   -Malicious IPs
   -Domains
   -File hashes
   -CVEs
-C2 Server - compromised system attacker uses to control malware while hiding their identity
-Trust levels - not all intel is equally trusted
-Sightings - tracking how many times IOC seen 

## How MISP connects to SOC
OPNsense -> Suricata -> Wazuh -> MISP -> Shuffle -> Dashboard

## Real World Application
Documented IOCs from real ransomware attack:
-Attacker IP flagged
-C2 domain shared
-Ransomware file hash shared
-CVE documented
