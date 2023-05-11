# OSCP Cheatsheet

This cheatsheet was created to help individuals who are new to boot2root style machines.

Cheatsheet is divided into four sections:

* [Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/tree/main/Enumeration)
* [Exploitation](https://github.com/shubhamagrawal7/OSCP-cheatsheet/tree/main/Exploitation)
* [Privilege Escalation](https://github.com/shubhamagrawal7/OSCP-cheatsheet/tree/main/Privilege%20Escalation)
* [Miscellaneous](https://github.com/shubhamagrawal7/OSCP-cheatsheet/tree/main/Miscellaneous)

## Enumeration

* The first thing anyone performs is Enumeration and starting with Network Scan. What could be better than [Nmap Scan](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/Nmap.md)
* Nmap scan will tell what services are open and according to that you can perform enumeration for those particular scans. For ex: If FTP is open then [FTP Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/FTP.md)
* If Nmap tells about Web service running, then you can run [Web Automated Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Web/Automated%20Enumeration.md) and [Web Manual Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Web/Manual%20Enumeration.md)
* **Quick Tip:** Keep noting down all the information you gather during the enumeration process. To open sublime text editor, use `subl` command.
* Wordlists and Password list can be found [here](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Miscellaneous/Important_Path.md#wordlists).
* Sometimes you will find images stored in the FTP directory or SMB shares, there is a possibility of hidden message in them. Use [Steganography Cheatsheet](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Miscellaneous/Steganography.md) to solve them.

## Exploitation

* After enumeration it is time to exploit. To try bruteforcing either a service password, like FTP, SSH, SMB, or a login password, use [Bruteforcing Cheatsheet](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Exploitation/Bruteforcing.md)
* If you are able to execute a command on the vulnerable machine, use [Reverse Shell cheatsheet](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Exploitation/ReverseShell.md) to get a reverse connection and further a stabilized shell.

## Privilege Escalation

* Once you have a reverse shell and you can execute OS commands on the vulnerable machine, use [Privilege Escalation cheatsheet](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Privilege%20Escalation/PrivilegeEscalation.md) to escalate access from a normal user to root user.
