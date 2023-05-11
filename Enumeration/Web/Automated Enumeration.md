# Web Enumeration with Nikto, Gobuster, and Wpscan

Web enumeration is the process of discovering and identifying web applications and their associated technologies and vulnerabilities. Here are some useful tools for conducting web enumeration.

## Nikto

Nikto is an open-source web server scanner that performs comprehensive tests against web servers for multiple items, including over 6700 potentially dangerous files and programs, outdated versions of over 1250 servers, and version-specific problems on over 270 servers. Here's an example of how to use Nikto:

```
nikto -h <target IP address> -p <target port>
```

* `-h <target IP address>: Specifies target IP address to scan.`
* `-p <target port>: Specifies the target port number to scan. If not specified, Nikto will default to port 80.`

## Gobuster

Gobuster is an open-source tool used for directory and DNS enumeration. It is designed to be used by penetration testers and web developers to find common flaws and vulnerabilities in web applications. Here are some examples of how to use Gobuster:

### Directory and File Enumeration

```
gobuster dir -u <target URL> -w <wordlist file path> -x <file extensions>
```

* `-u <target URL>: Specifies the target URL of the website or web application.`
* `-w <wordlist file path>: Specifies the path to the wordlist file. Ex: /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt`
* `-x <file extensions>: Specifies the file extensions to be used during the enumeration. Ex: -x php,txt,html would search for directories or files with the extensions .php, .txt, and .html.`

### Virtual Host Enumeration

```
gobuster vhost -u <target URL> -w <wordlist file path>
```

* `-u <target URL>: Specifies the target URL of the website or web application.`
* `-w <wordlist file path>: Specifies the path to the wordlist file. Ex: /usr/share/wordlists/dirbuster/directory-2.3-medium-list.txt`

## Bruteforce login password

Bruteforcing is a technique used to crack passwords by guessing multiple combinations of characters until the correct password is found. This technique can be used to gain unauthorized access to a web application by guessing the login password.

**Example: To conduct a bruteforce attack, use a tool such as Hydra or Burp Suite Intruder.**

**For example, to bruteforce the login page of a web application, use the following command with Hydra: `hydra -l username -P /path/to/passwords.txt example.com http-post-form "/login.php:username=^USER^&password=^PASS^:Invalid username or password"`.**

This command will use the username `username` and passwords from the file `/path/to/passwords.txt` to bruteforce the login page at `example.com/login.php`.


## Wpscan

Wpscan is a WordPress vulnerability scanner. It can be used to scan WordPress installations for known vulnerabilities, plugins, and themes. Here are some examples of how to use Wpscan:

### User Enumeration

```
wpscan --url <target URL> --enumerate
```

The above syntax will enumerate everything for a wordpress site like: Installed Plugins, TimThumbs, Usernames, Wordpress Version etc.
