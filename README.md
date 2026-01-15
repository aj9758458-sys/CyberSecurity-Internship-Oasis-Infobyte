

Network Scanning with Nmap

Project Objective

The goal of this project was to perform a basic network scan on a local machine to identify open ports, understand the services running on them, and document the security implications.

 Methodology
Tool: Nmap 7.98
Target:Localhost (127.0.0.1)
Command Used:`nmap localhost`


 Scan Results Analysis


+------+-------+---------------+---------------------------------------------------------------------------------------------+
| Port | State | Service       | Significance                                                                                 |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 80   | Open  | HTTP          | Indicates a web server is running on the system, commonly used for hosting web applications |
|      |       |               | or local services.                                                                           |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 135  | Open  | MSRPC         | Used by Windows for Remote Procedure Calls. Essential for system communication but can be    |
|      |       |               | targeted if exposed.                                                                         |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 445  | Open  | Microsoft-DS  | Supports SMB file sharing in Windows. This port is often targeted by malware and should be   |
|      |       |               | secured.                                                                                     |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 1521 | Open  | Oracle        | Default listener port for Oracle Database, indicating a database service running locally.   |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 3306 | Open  | MySQL         | Default port for MySQL database access. Unauthorized exposure can lead to data breaches.     |
+------+-------+---------------+---------------------------------------------------------------------------------------------+
| 5500 | Open  | Hotline       | Often associated with Oracle Enterprise Manager or related management services.              |
+------+-------+---------------+---------------------------------------------------------------------------------------------+



Conclusion

The scan successfully identified multiple active services on the local machine, including a web service (HTTP), database services (MySQL and Oracle), and critical Windows networking services (MSRPC and SMB). From a security perspective, ports such as **445, 3306, and 1521** should be properly secured and restricted to trusted users only. Running unnecessary services should be avoided to reduce the attack surface of the system.


