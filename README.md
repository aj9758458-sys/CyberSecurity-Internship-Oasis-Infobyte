 Network Scanning with Nmap

 Project Objective


This project aimed to carry out a basic network scan on a local system in order to detect open ports, identify the services operating on those ports, and analyze their security impact.

Methodology
 Tool: Nmap 7.98
 
Target: Localhost (127.0.0.1)

Command Used:`nmap localhost`

 Scan Results Analysis

| Port | State | Service      | Significance                                                                                                    |
| :--- | :---- | :----------- | :-------------------------------------------------------------------------------------------------------------- |
| 80   | Open  | HTTP         | Shows that a web server is active on the system and may be used for hosting websites or local web applications. |
| 135  | Open  | MSRPC        | Utilized by Windows systems for Remote Procedure Call services and essential system operations.                 |
| 445  | Open  | Microsoft-DS | Enables SMB-based file sharing in Windows environments and is frequently targeted by attacks.                   |
| 1521 | Open  | Oracle       | Standard port for Oracle Database listener, indicating an active database service.                              |
| 3306 | Open  | MySQL        | Default port for MySQL database connections, which can be exploited if not properly secured.                    |
| 5500 | Open  | Hotline      | Commonly linked to Oracle Enterprise Manager or related administrative services.                                |

Conclusion


The scan successfully identified multiple active services on the local machine, including a web service (HTTP), database services (MySQL and Oracle), and critical Windows networking services (MSRPC and SMB). From a security perspective, ports such as 445, 3306, and 1521 should be properly secured and restricted to trusted users only. Running unnecessary services should be avoided to reduce the attack surface of the system.
