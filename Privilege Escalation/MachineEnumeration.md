# Machine Enumeration for Privilege Escalation

During the process of Privilege Escalation, it is essential to perform thorough machine enumeration to gather information about the target system. This information can help identify potential vulnerabilities, misconfigurations, or weak points that can be exploited to escalate privileges. The following are some techniques and tools that can be used for machine enumeration:

## 1. System Information

- **uname** - Check the system information such as kernel version and architecture.
  Example: `uname -a`

- **cat /etc/os-release** - View the operating system release information.
  Example: `cat /etc/os-release`

- **lsb_release -a** - Display LSB (Linux Standard Base) information.
  Example: `lsb_release -a`

- **hostname** - Determine the hostname of the system.
  Example: `hostname`

## 2. User and Group Enumeration

- **id** - Get the current user and group information.
  Example: `id`

- **cat /etc/passwd** - View the user accounts on the system.
  Example: `cat /etc/passwd`

- **cat /etc/group** - List the groups on the system.
  Example: `cat /etc/group`

- **getent passwd** - Retrieve user account details from the system databases.
  Example: `getent passwd`

## 3. Network Information

- **ifconfig** - Display network interface configuration and IP addresses.
  Example: `ifconfig`

- **ip addr** - View the network interfaces and their configurations.
  Example: `ip addr`

- **netstat -tuln** - List open ports and associated services.
  Example: `netstat -tuln`

- **route** - Show the IP routing table.
  Example: `route`

## 4. Running Processes

- **ps aux** - List all running processes and their details.
  Example: `ps aux`

- **top** - Monitor real-time system processes, CPU usage, and memory usage.
  Example: `top`

- **pstree** - Display running processes in a tree-like format.
  Example: `pstree`

## 5. Installed Software and Packages

- **dpkg -l** - List installed packages on Debian-based systems.
  Example: `dpkg -l`

- **rpm -qa** - Display installed packages on RPM-based systems.
  Example: `rpm -qa`

- **ls -l /usr/bin /usr/sbin | more** - Browse common binaries and executables.
  Example: `ls -l /usr/bin /usr/sbin | more`

## 6. File System and Permissions

- **df -h** - View disk space usage and available file systems.
  Example: `df -h`

- **mount** - List mounted file systems.
  Example: `mount`

- **ls -al /root** - Check the permissions and content of the root directory.
  Example: `ls -al /root`

- **ls -al /home** - Explore user home directories and their permissions.
  Example: `ls -al /home`
