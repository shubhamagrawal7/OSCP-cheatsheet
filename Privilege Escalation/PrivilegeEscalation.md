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
   - Online Resource: [https://book.hacktricks.xyz/linux-unix/privilege-escalation#passwords-inetcshadow](https://book.hacktricks.xyz/linux-unix/privilege-escalation#passwords-inetcshadow)

3. **Check if Passwd and Shadow Files are Writable:**
   - Checking if the `/etc/passwd` and `/etc/shadow` files are writable to modify user accounts or credentials.
   - Example: `ls -l /etc/passwd /etc/shadow`
   - Online Resource: [https://book.hacktricks.xyz/linux-unix/privilege-escalation#writable-etc-passwd](https://book.hacktricks.xyz/linux-unix/privilege-escalation#writable-etc-passwd)

4. **Check for SUID/SGID Bits Enabled Files:**
   - Identifying files with SUID (Set User ID) or SGID (Set Group ID) permissions that can be leveraged to escalate privileges.
   - Example: `find / -perm -4000 -type f -exec ls -l {} \;`
   - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid)

5. **Check for OS, Kernel Version Exploits:**
   - Searching for known OS or kernel vulnerabilities using tools like `searchsploit` to find relevant exploits.
   - Example: `searchsploit linux kernel 3.10`
   - Online Resource: [https://www.exploit-db.com/](https://www.exploit-db.com/)

6. **Check History Command:**
   - Inspecting the command history of the current user to find previously executed commands or sensitive information.
   - Example: `history`
   - Online Resource: [https://book.hacktricks.xyz/linux-unix/privilege-escalation#sudo-history](https://book.hacktricks.xyz/linux-unix/privilege-escalation#sudo-history)

7. **Check for Binaries with Sudo Privileges:**
   - Using the `sudo -l` command to identify binaries that can be executed with elevated privileges.
   - Example: `sudo -l`
   - Online Resource: [https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid](https://book.hacktricks.xyz/linux-hardening/privilege-escalation#sudo-and-suid)

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
