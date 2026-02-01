# SOC-HOME-SETUP
indroduction                                                                 
This project establishes a Security Operations Center (SOC) home lab environment to emulate real-world cyberattacks and detection capabilities using Splunk, incorporating log forwarding, attack simulation, and alert generation to demonstrate comprehensive security monitoring and incident detection.  

Lab Overview :

Attacker: A Kali Linux system, serving as the dedicated platform for executing security assessments and simulated attacks.                                        
Victim : An Ubuntu server configured with multiple services, including a deliberately vulnerable web application, SSH, and FTP, to act as the target for the offensive host.
Monitoring Tool: A Windows server running Splunk Enterprise professional, which functions as the central SIEM for log aggregation, analysis, and alerting.  

Technologies Used :

SIEM Platform: Splunk Enterprise, deployed on a Windows server.
Log Agent: Splunk Universal Forwarder, installed on the Ubuntu target machine to forward logs.
Attack Simulation: A Kali Linux machine for conducting offensive security operations.
Virtualization Environment: VirtualBox or an equivalent hypervisor to host the virtual machines.
Target Services: Apache2 web server, vsftpd for FTP, and a custom login page on the Ubuntu target.    

Implementation Procedure: 

1.Configure Ubuntu (Target)-
.Install Apache, FTP, SSH and a custom vulnerable login page.
.Install and configure the Splunk Universal Forwarder.
.Forward /var/log/auth.log and /var/log/apache2/* to the Splunk server.

2.Configure Splunk Server (Windows)
.Install Splunk Enterprise.
.Configure inputs for receiving logs from the forwarder.
.Create dashboards and alerts.

3.Launch Attacks from Kali
.SSH brute-force using hydra.
.Web login brute-force using hydra or wfuzz.
.Web directory enumeration using gobuster.
.FTP anonymous login attempts.
.Trigger Windows failed logins manually for detection.     
       
 Detection Rules: 
 
.SSH Brute Force Detection
.Web Login Brute Force Detection
.Web Directory Enumeration
.FTP Anonymous Login Detection
.Windows Failed Login Attempts

Screenshot

