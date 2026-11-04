# Escalate My Privileges: Bluemoon – Penetration Testing Writeup

## Objective
Fully compromise the vulnerable machine Bluemoon (VulnHub, "Escalate My Privilege: 1") by gaining initial access and escalating privileges from a low-privilege user to root.

## Lab Setup
The Bluemoon VM (.ova from VulnHub) was imported into Oracle VirtualBox and run alongside the Kali Linux attacker machine. Both VMs were set to a Host-only Adapter so they share the same isolated network.

- Target (Bluemoon) IP: 192.168.56.104
- Attacker (Kali) IP: 192.168.56.102

Connectivity was confirmed with `ping 192.168.56.104`, which returned 0% packet loss.

## Reconnaissance
A full port scan was run against the target using Nmap.

![Nmap scan results](screenshots/nmap-scan)
![Initial access via phpbash webshell](screenshots/initial-access)
![Root access confirmed](screenshots/root-access)
