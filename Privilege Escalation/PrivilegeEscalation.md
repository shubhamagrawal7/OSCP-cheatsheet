# Privilege Escalation Techniques

Privilege Escalation is the process of gaining higher-level permissions or privileges on a system or network. This cheatsheet provides an overview of Privilege Escalation techniques, examples, and online resources.

## Privilege Escalation Techniques

1. **Linpeas:**
   - Using Linpeas script to perform automated privilege escalation checks on Linux systems.
   - Example: `./linpeas.sh`
   - Online Resource: [https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS](https://github.com/carlospolop/privilege-escalation-awesome-scripts-suite/tree/master/linPEAS)

2. **Check if Shadow File is Readable:**
   - Checking if the `/etc/shadow` file is readable to obtain hashed user passwords.
   - Example: `cat /etc/shadow`
   - Download shadow file to your local machine by copying the shadow file to `/tmp` and starting a python server `python -m http.server <port_number>`
   - On your local machine, go to `http://<vulnerable-machine-ip>:<port_number>/<shadow-file>`
   - On your local machine, use John The Ripper to crack shadow file hashes: `john --wordlist=<path-to-wordlist> <shadow_file>`
   - Use the cracked password to login to user/root accounts on the vulnerable machine.

3. **Check if Passwd and Shadow Files are Writable:**
   - Checking if the `/etc/passwd` and `/etc/shadow` files are writable to modify user accounts or credentials.
   - Example: `ls -l /etc/passwd /etc/shadow`
   - If Passwd file is writable, use this resource: [Writable Passwd File](https://steflan-security.com/linux-privilege-escalation-writable-passwd-file/)
   - If Shadow file is writable, use this resource: [Writable Shadow File](https://blog.geoda-security.com/2019/02/privilege-escalation-exploiting-write.html)

4. **Exploit Sudo Privileges:**
    - Using the `sudo -l` command to check sudo privileges for the current user.
    - Example: `sudo -l`
    - Online Resource: [Exploiting Binaries with Sudo Privileges](https://www.hackingarticles.in/linux-privilege-escalation-using-exploiting-sudo-rights/)

5. **Check for SUID/SGID Bits Enabled Files:**
   - Identifying files with SUID (Set User ID) or SGID (Set Group ID) permissions that can be leveraged to escalate privileges.
   - Example: `find / -perm -4000 -type f 2>/dev/null`
   - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid)

6. **Check for OS, Kernel Version Exploits:**
   - Searching for known OS or kernel vulnerabilities using tools like `searchsploit` to find relevant exploits.
   - Example: `searchsploit linux kernel 3.10`
   - Online Resource: [https://www.exploit-db.com/](https://www.exploit-db.com/)

7. **Check History Command:**
   - Inspecting the command history of the current user to find previously executed commands or sensitive information.
   - Example: `history`

8. **Cron Jobs:**
   - Inspecting cron jobs to identify any scheduled tasks executed with elevated privileges.
   - Example: `crontab -l`
   - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation#scheduled-cron-jobs](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#scheduled-cron-jobs)

9. **Linux Capabilities:**
   - Checking for Linux capabilities assigned to binaries, which can provide privileged access.
   - Example: `getcap -r / 2>/dev/null`
   - Online Resource: [https://book.hacktricks.xyz/linux-unix/privilege-escalation#capabilities](https://book.hacktricks.xyz/linux-unix/privilege-escalation#capabilities)

10. **Using Network File Sharing:**
    - Exploiting network file sharing misconfigurations or vulnerabilities to gain unauthorized access.
    - Example: Exploiting misconfigured NFS (Network File System) exports.
    - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation/nfs-no_root_squash-misconfiguration-pe](https://book.hacktricks.xyz/linux-hardening/privilege-escalation/nfs-no_root_squash-misconfiguration-pe)

11. **Creating Own Binary and Changing PATH Environment Variable:**
    - Creating a custom binary or script and manipulating the PATH environment variable to execute it with higher privileges.
    - Example: Creating a malicious `ls` binary and adding its path to the beginning of the PATH variable.
    - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation#writable-path-abuses](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#writable-path-abuses)

## Additional Resources

- GTFOBins: [https://gtfobins.github.io/](https://gtfobins.github.io/)
- Windows Privilege Escalation Commands: [https://book.hacktricks.xyz/windows/windows-local-privilege-escalation](https://book.hacktricks.xyz/windows/windows-local-privilege-escalation)
- Linux Privilege Escalation Scripts: [https://github.com/diego-treitos/linux-smart-enumeration](https://book.hacktricks.xyz/linux-hardening/privilege-escalation)
