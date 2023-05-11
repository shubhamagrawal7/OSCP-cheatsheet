# FTP Enumeration

After Nmap scan, if you see that FTP service is open. You can use the following commands to do some checks.

* Connect to FTP service
* Check if Anonymous Login is Enabled or not.
* If enabled, check every file and folder, download each file and also look for hidden files.

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
