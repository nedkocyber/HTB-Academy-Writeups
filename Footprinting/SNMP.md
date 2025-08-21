# SNMP


What is SNMP (Simple Network Management Protocol)?

SNMP is a network protocol used for:

Monitoring devices such as routers, servers, IoT systems, etc.
Managing and remotely modifying device configurations


How Does It Work?

Operates over UDP port 161 for queries (requests)
Uses UDP port 162 for SNMP traps (alerts or notifications sent from device to management system)
Interacts with SNMP objects, each identified by a unique OID (Object Identifier)
These objects are defined in MIB (Management Information Base) files – standardized text files describing the structure and data available for SNMP access

Using the basic command snmpwalk -v2c -c public 10.129.119.5 we were able to retrieve a large amount of valuable information from the SNMP service, which can aid in further enumeration and exploitation.


<img width="499" height="242" alt="image" src="https://github.com/user-attachments/assets/edff590c-eafe-43ea-b41b-a51b3c2ae2f6" />

For the third task, we can either use grep "HTB" <output-file> if the output has been saved to a file, or simply manually scroll through the output and locate the flag visually.


<img width="840" height="152" alt="image" src="https://github.com/user-attachments/assets/6f3ec798-ad4d-4e95-b982-0ced4ab46043" />
