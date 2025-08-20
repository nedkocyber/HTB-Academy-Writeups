# SMB

<img width="1034" height="462" alt="image" src="https://github.com/user-attachments/assets/59e9ad79-2ffb-446a-b932-1fae611bb035" />

We began with a basic Nmap scan to identify open ports and determine which services are running on the target system.

<img width="1046" height="692" alt="image" src="https://github.com/user-attachments/assets/de61ffcd-3638-4caf-b147-c0e271cc8630" />

We connected to the SMB share named sambashare and successfully retrieved the flag to our local machine.

<img width="436" height="88" alt="image" src="https://github.com/user-attachments/assets/de78ec9c-4f2c-44ff-b99b-273b4a22ab1c" />

rpcclient is a command-line utility used to interact with Windows or Samba servers over the RPC (Remote Procedure Call) protocol. It’s particularly useful during enumeration in penetration testing or system administration.

With rpcclient, you can:

 - Enumerate users on the remote system
 - Identify the domain the server belongs to
 - List available shared folders (shares)
 - Gather information about groups and permissions

<img width="281" height="80" alt="image" src="https://github.com/user-attachments/assets/c58d861e-0c67-4253-abec-a2e962cdded7" />


<img width="1033" height="426" alt="image" src="https://github.com/user-attachments/assets/0fbf09b8-c2c3-4528-875d-42758b1aa59d" />

