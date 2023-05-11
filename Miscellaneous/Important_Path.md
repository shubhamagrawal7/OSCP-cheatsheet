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
  - - On the local machine, send the file: ``` nc <target IP> <port> <file_to_send> ```

* Another example  
