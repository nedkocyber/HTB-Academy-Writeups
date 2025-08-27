# Cron Job Abuse

We begin with -->  find / -path /proc -prune -o -type f -perm -o+w 2>/dev/null  this command searches the entire filesystem (starting from /) for world-writable files.

<img width="1044" height="161" alt="image" src="https://github.com/user-attachments/assets/069d6357-698c-4072-9d9a-86a2d0907035" />

During enumeration, we discover the file backup.sh, which is world-writable while being executed with root privileges. This misconfiguration allows any user on the system to modify the script’s contents. By injecting malicious commands into backup.sh, we can leverage its execution to escalate privileges and obtain a root shell.

<img width="665" height="116" alt="image" src="https://github.com/user-attachments/assets/871d6921-ea9a-44d6-a4a9-256834d5ca2e" />

Here we add a reverse shell

<img width="843" height="146" alt="image" src="https://github.com/user-attachments/assets/1a756a7e-dda6-4060-8851-80012b4baa6d" />

The critical aspect of this misconfiguration is that backup.sh runs periodically with root privileges, regardless of whether it is triggered manually or executed automatically by the system (e.g., via a scheduled task such as cron).

To exploit this, we insert a reverse shell payload into backup.sh, start a Netcat listener on our attacking machine, and wait for the script to execute. Once it runs, the payload is executed as root, providing us with a privileged shell.

<img width="937" height="214" alt="image" src="https://github.com/user-attachments/assets/388f48c3-2c6c-4ce8-a65c-94812986f6f1" />

<img width="454" height="142" alt="image" src="https://github.com/user-attachments/assets/9ae74f7c-7b39-418c-aa7e-35596a117d7b" />
