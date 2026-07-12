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

10. ## Findings

During the assessment, the following observations were made:

- Apache Tomcat was successfully deployed on Ubuntu Server.
- Port **8080** was open and accessible.
- Nmap identified the Apache Tomcat service.
- Gobuster discovered the following directories:
  - `/docs`
  - `/examples`
  - `/manager`
  - `/host-manager`
- Nikto identified:
  - Missing X-Frame-Options header
  - Missing X-Content-Type-Options header
  - Exposed Tomcat Manager interface
  - Exposed Host Manager interface
  - Multiple HTTP methods enabled
    ## Recommendations

- Configure the X-Frame-Options header to reduce clickjacking risk.
- Configure the X-Content-Type-Options header to prevent MIME type sniffing.
- Restrict access to the Tomcat Manager and Host Manager applications.
- Disable unnecessary HTTP methods if they are not required.
- Remove example applications and documentation from production servers.
- Keep Apache Tomcat updated to the latest stable version.
