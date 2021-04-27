| **Command**   | **Description**   |
| --------------|-------------------|
| **Web Enumeration** |
| `gobuster dir -u <ip> -w <list>` | directory scan |
| `gobuster dns -d <address> -w <list>` | subdomain scan |
| `curl -IL <ip>` | get website banner |
| `curl <ip>/robots.txt` | potentially get some directories |