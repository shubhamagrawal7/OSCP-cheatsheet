# SMB Enumeration

After performing Nmap scan, if you see SMB port is open, then you can use the following commands to enumerate this service.
* The first thing to look for is open shares. It can be done using [SMB Version Detection](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/SMB.md#smb-version-detection)
* After finding the list of shares, its time to connect to each one of them anonymously (unless you have the password for the shares). Use [SMB Auth Enum](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/SMB.md#smb-authentication-enumeration) and do not give any username and password with it.
* Traverse through the shares using `ls` command and download them to your local machine using `get` command.
* Your last resort would be to try [bruteforcing](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/SMB.md#smb-brute-force-attacks) SMB shares

## SMB Version Detection

To determine the SMB version running on the target system, you can use the `smbclient` tool:

```
smbclient -L <target>
```

This command will list the shares available on the target system, as well as the SMB version being used.

## SMB Authentication Enumeration

If the target system is using SMB2 or later, it may be vulnerable to an authentication bypass attack. You can use the `smbclient` tool to check for this vulnerability:

```
smbclient //<target>/<share> -U "username%password"
```

Replace `<target>` with the IP address or hostname of the target system, `<share>` with the name of a share on the target system, `<username>` with a username to test, and `<password>` with a password to test.

If the authentication is successful, you will be prompted with an `smb: \>` prompt, indicating that you have access to the share.

## SMB Brute-Force Attacks

If you have a list of usernames and passwords to test, you can use a tool like `hydra` to perform a brute-force attack against the target system:

```
hydra -l <username> -P <password list> <target> smb
```

Replace `<username>` with a username to test, `<password list>` with the path to a file containing a list of passwords to try, and `<target>` with the IP address or hostname of the target system.

# Enum4linux

Enum4linux is a tool used for enumerating information from Windows and Samba systems. It can be used to extract various types of information, including user and group details, share and disk information, and password policies.

## Syntax

```
enum4linux -a <target IP>
```

The above syntax will perform all the scans for a target IP.
