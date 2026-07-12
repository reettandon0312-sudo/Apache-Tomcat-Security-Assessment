Apache-tomcat-security-assessment

## Project Overview

This project demonstrates a security assessment of an Apache Tomcat web server hosted on Ubuntu Server in a VirtualBox lab environment. The assessment was performed from a Kali Linux machine using Nmap, Gobuster, and Nikto to identify exposed services, hidden directories, and common web server security issues.
## Lab Environment

| Machine | Role |
|----------|------|
| Kali Linux | Attacker Machine |
| Ubuntu Server | Target Machine |
| Apache Tomcat 10.1.57 | Web Server |
| VirtualBox | Virtualization Platform |
## Tools Used

- Kali Linux
- Ubuntu Server
- Apache Tomcat 10.1.57
- VirtualBox
- Nmap
- Gobuster
- Nikto
- OpenJDK 25

  ## Project Workflow

1. Set up Ubuntu Server in VirtualBox.
2. Installed OpenJDK 25.
3. Installed Apache Tomcat 10.1.57.
4. Configured Host-Only networking.
5. Verified connectivity between Kali and Ubuntu.
6. Performed Nmap scanning.
7. Enumerated directories using Gobuster.
8. Assessed the web server using Nikto.
9. Analyzed the findings and documented recommendations.
