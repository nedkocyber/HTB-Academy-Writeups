# IPMI

IPMI (Intelligent Platform Management Interface)

IPMI is a standard for hardware-based server management, allowing administrators to:
Monitor and control the system even when it is powered off
Remotely restart, shut down, or reinstall the operating system
Operate independently of the BIOS, CPU, OS, and hard disk

Common Use Cases:

Before the OS is loaded – to modify BIOS settings remotely.
When the host is powered off – for remote power-on or reboot.
After a system crash – to access the system even when the OS is unresponsive.

IPMI Can Monitor:

Temperature
Voltage levels
Fan and power supply status
Hardware inventory
System event logs (SEL)
Alerts via SNMP


<img width="1047" height="441" alt="image" src="https://github.com/user-attachments/assets/0a798198-def7-451d-ac8b-7b87b02ef71c" />

We used msfvenom to craft a payload and exploit the service, which allowed us to retrieve a hashed password along with a username. Then, using Hashcat, we successfully cracked the password.

<img width="1047" height="65" alt="image" src="https://github.com/user-attachments/assets/8ec43303-36da-43a5-9d39-c80ad2cbe814" />

<img width="1044" height="57" alt="image" src="https://github.com/user-attachments/assets/1c4af2da-9c6b-4ae5-a128-96fb23eaa52d" />
