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
* Nmap will help know what service is running on every port. If you find a Web service running, then you can run [Web Automated Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Web/Automated%20Enumeration.md) and [Web Manual Enumeration](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Web/Manual%20Enumeration.md)


## Exploitation


## Privilege Escalation

After you have gained access to the machine, its time to [Privilege Escalate]()
The user flags can mostly be found in the user home directories with the name user.txt.
