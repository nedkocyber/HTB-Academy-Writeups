# Logrotate

We start the lab by deploying the logrotten exploit on our Kali Linux machine, ensuring all dependencies are in place and the environment is ready for testing, and then sending it over to the target machine and compiling it there for execution.

<img width="727" height="408" alt="image" src="https://github.com/user-attachments/assets/b0e756a2-450b-489c-8d8a-0faf84305802" />

Next, we create a reverse shell payload, preparing it to establish a connection back to our Kali machine once executed on the target system.

<img width="715" height="17" alt="image" src="https://github.com/user-attachments/assets/dde0daf1-0fc2-4afe-9df5-6541ddbf115e" />

./logrotten runs the LogRotten exploit.
-p ./payload specifies the payload file to inject.
~/backups/access.log tells LogRotten which log file to monitor.

Effect: LogRotten watches the log file and triggers the payload when changes are detected. Combining the two commands with && ensures the log file is ready before LogRotten starts monitoring.

<img width="900" height="82" alt="image" src="https://github.com/user-attachments/assets/cab82a9c-4604-4c56-a403-453aa01e4b6e" />

Before running the exploit, start a Netcat listener on your Kali machine to catch the incoming connection. Once the exploit is triggered, we should receive a root shell immediately. Be prepared to execute cat flag.txt quickly, as the shell will remain open for only a few seconds.

<img width="481" height="142" alt="image" src="https://github.com/user-attachments/assets/2610cda0-9f14-4b9f-861d-42b9a054ae82" />
