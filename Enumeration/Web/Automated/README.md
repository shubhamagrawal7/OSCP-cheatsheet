# Web Enumeration with Nikto, Gobuster, Wpscan, and Dirb

Web enumeration is the process of discovering and identifying web applications and their associated technologies and vulnerabilities. Here are some useful tools for conducting web enumeration.

## Nikto

Nikto is an open-source web server scanner that performs comprehensive tests against web servers for multiple items, including over 6700 potentially dangerous files and programs, outdated versions of over 1250 servers, and version-specific problems on over 270 servers. Here's an example of how to use Nikto:

nikto -h <target IP address> -p <target port>

## Gobuster

Gobuster is an open-source tool used for directory and DNS enumeration. It is designed to be used by penetration testers and web developers to find common flaws and vulnerabilities in web applications. Here are some examples of how to use Gobuster:

### Directory Enumeration

gobuster dir -u <target URL> -w <wordlist file path> -x <file extensions> -t <number of threads>

### File Enumeration

gobuster dir -u <target URL> -w <wordlist file path> -x <file extensions> -t <number of threads> -s <status codes> -k

### Virtual Host Enumeration

gobuster vhost -u <target URL> -w <wordlist file path> -t <number of threads>

## Wpscan

Wpscan is a WordPress vulnerability scanner. It can be used to scan WordPress installations for known vulnerabilities, plugins, and themes. Here are some examples of how to use Wpscan:

### User Enumeration

wpscan --url <target URL> --enumerate u

### Password Bruteforcing

wpscan --url <target URL> --wordlist <wordlist file path> --username <username> --threads <number of threads> --passwords <passwords file path>

## Dirb

Dirb is a web content scanner that looks for hidden directories on web servers. It is designed to be fast and effective, making it a popular choice for web enumeration. Here's an example of how to use Dirb:

### Directory Enumeration

dirb <target URL> <wordlist file path>
