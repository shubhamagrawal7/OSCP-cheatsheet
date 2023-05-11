# FTP Enumeration

After Nmap scan, if you see that FTP service is open. You can use the following commands to do some checks.

* Connect to FTP service
* Check if Anonymous Login is Enabled or not.
* If enabled, check every file and folder, download each file and also look for hidden files.
* The last resort if not able to authenticate will be [brute-forcing](https://github.com/shubhamagrawal7/OSCP-cheatsheet/blob/main/Enumeration/Network/FTP.md#brute-force-attacks)

## Banner Grabbing

To determine the FTP server version and other information, you can use a tool like `nc` or `ftp` to connect to the FTP server and retrieve the banner:

```
nc <target> 21
```

```
ftp <target>
```

## Anonymous FTP Access

If anonymous FTP access is enabled on the server, you can connect to it with the username `anonymous` and a blank password:

```
ftp <target>
```

username: anonymous

password:

Once you have logged in, you can use FTP commands like `ls` to list files and directories, `get <file-name>` to download files and `put <file-name>` to upload files.

## Brute-Force Attacks

If anonymous FTP access is not enabled, you can try brute-forcing FTP credentials using a tool like `hydra`:

```
hydra -l <username> -P <password list> ftp://<target>
```

Replace `<username>` with the username you want to brute-force, `<password list>` with the path to a file containing a list of passwords to try, and `<target>` with the IP address or domain name of the FTP server. If you want to use rockyou.txt passwordlist, the path to the list will be: `/usr/share/wordlists/rockyou.txt`
