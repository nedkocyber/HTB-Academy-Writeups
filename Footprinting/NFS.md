# NFS

Ports 111 and 2049 are the equivalents of SMB for Linux and Unix-based systems, providing services like RPC and NFS respectively.

<img width="1154" height="823" alt="image" src="https://github.com/user-attachments/assets/1d2efd91-8dae-4a2a-a123-1b9ae56ecc41" />
<img width="896" height="539" alt="image" src="https://github.com/user-attachments/assets/4def5928-7d27-4936-815e-6fe637dce53e" />

Both ports are open, so we use the showmount command to list all accessible NFS shares available to us.

<img width="441" height="131" alt="Screenshot 2025-08-20 175649" src="https://github.com/user-attachments/assets/3bdf857a-7da8-4016-a00b-9b12f60aeaab" />


<img width="779" height="582" alt="image" src="https://github.com/user-attachments/assets/112d84a5-1253-409a-9c66-1d9bade14a85" />

It mounts an NFS (Network File System) share from the remote server (10.129.14.128) to a local directory (./target-NFS/), using the following parameters:

Component	and Description
sudo	-> Executes the command with administrative (root) privileges.
mount ->	Command used to mount a filesystem.
-t nfs ->	Specifies the type of filesystem – in this case, NFS.
10.129.14.128:/ ->	Server address and root of the NFS shared export.
./target-NFS/	 -> Local directory where the NFS share will be mounted.
-o nolock ->	Disables file locking (useful when lockd service is not running).

<img width="724" height="255" alt="image" src="https://github.com/user-attachments/assets/ae17bf7e-7dad-4354-abb7-cee55e98d05a" />
