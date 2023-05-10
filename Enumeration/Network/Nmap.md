# Nmap and Useful Commands

## Directly use this or follow the below guide

`nmap -sC -sV -T5 -A -p- <targetIP>`

`-sC: Runs the default script scan on the target system.

-sV: Performs version detection on the target system, which can help identify which services are running and what vulnerabilities they may be susceptible to.

-T5: Sets the timing template to "Insane" which means that Nmap will send probes at a very high speed.

 -A: This option will enable OS detection, version detection, script scanning, and traceroute.
 
-p-: This option specifies that all ports should be scanned, rather than just the common ports.`

## Basic Nmap Commands

Here are some basic Nmap commands that are useful for performing basic reconnaissance on a target:

`nmap <target>`

This command will perform a basic scan of the target system and report back which ports are open and what services are running on those ports.

`nmap -sS <target>`

This command will perform a TCP SYN scan, which is a stealthy scan that attempts to avoid detection by firewalls and intrusion detection systems.

`nmap -sU <target>`

This command will perform a UDP scan, which is useful for identifying open UDP ports that may be vulnerable to attack.

## Advanced Nmap Commands

Here are some advanced Nmap commands that are useful for performing more in-depth reconnaissance and vulnerability assessment:

`nmap -A <target>`

This command will perform an aggressive scan that includes OS detection, version detection, script scanning, and traceroute.

`nmap -sV <target>`

This command will perform version detection on the target system, which can help you identify which services are running and what vulnerabilities they may be susceptible to.

`nmap --script <script> <target>`

This command will run a specific Nmap script against the target system. Nmap scripts are pre-written scripts that automate various tasks, such as vulnerability scanning, service enumeration, and exploitation.
