# Linux Local Privilege Escalation - Skills Assessment

## Flag 1

From the command history, we can see that the user previously attempted to access the flag, but their attempts were blocked or misconfigured, preventing access.

<img width="854" height="454" alt="image" src="https://github.com/user-attachments/assets/52d52a74-dcb8-4630-b256-c775b8cd8310" />

In the screenshot, we can see that the file is hidden in the first path, indicating it is not immediately visible in the directory listing.

<img width="967" height="144" alt="image" src="https://github.com/user-attachments/assets/b215e89f-2ab5-43f3-8bcf-64c726559762" />

<img width="528" height="52" alt="image" src="https://github.com/user-attachments/assets/79e88292-e6a6-4eba-9660-549715e3fee0" />

## Flag 2

Here, we can see that the user started a session with the database and a tmux session, including their SSH password.

<img width="692" height="291" alt="image" src="https://github.com/user-attachments/assets/4fb2312f-64c6-4b2e-be88-8e1c42a4dff7" />

<img width="824" height="767" alt="image" src="https://github.com/user-attachments/assets/6966b9ed-b4ed-4990-b79a-abad3c8d109e" />

We then log in via SSH and retrieve the second flag.

<img width="955" height="592" alt="image" src="https://github.com/user-attachments/assets/00dc73bf-3f66-49bc-9617-4c8085d0b57c" />


## Flag 3

From Barry’s command history, we can also see that he accessed /var/log, and there we find the third flag.

<img width="1036" height="605" alt="image" src="https://github.com/user-attachments/assets/6bb511a1-26a1-4f93-a038-96abbbe4eaad" />


## Flag 4

find -name "*.bak" – searches the current directory and all subdirectories for files ending with .bak (typically backup files).

<img width="672" height="71" alt="image" src="https://github.com/user-attachments/assets/d7778e25-6517-43ff-8c59-be9349fc167f" />

In this file, we find a username and password, and we also notice that there appears to be a web application running. We proceed by navigating to it on port 8080 to explore further.

<img width="1054" height="802" alt="image" src="https://github.com/user-attachments/assets/24b91197-b8dc-474b-80db-ea504ea60b70" />

<img width="942" height="361" alt="image" src="https://github.com/user-attachments/assets/ad3ebe57-4cd6-4b74-8792-8bfe7cbbb826" />

After logging in, we observe that the application allows file uploads. We then create a reverse shell using msfvenom and upload it to the server to gain remote access.

<img width="1038" height="92" alt="image" src="https://github.com/user-attachments/assets/d8973fda-0be6-4db6-8ec7-737ce349657b" />

Once the reverse shell is uploaded, we start a Netcat listener on our machine and execute the uploaded payload, which gives us a shell on the target server.

<img width="693" height="174" alt="image" src="https://github.com/user-attachments/assets/d5897ae8-671e-4a15-ab72-7dcf3a8b3330" />

<img width="857" height="401" alt="image" src="https://github.com/user-attachments/assets/26ffe9d7-1150-4054-945d-a25282e523c7" />

## Flag 5

This spawns a fully interactive Bash shell, allowing us to execute commands more effectively on the target system.

<img width="570" height="48" alt="image" src="https://github.com/user-attachments/assets/fea1492d-a955-41ee-8d7a-57bca5237adc" />

Running sudo -l reveals valuable information: we are allowed to execute /usr/bin/busctl with elevated privileges

<img width="1018" height="200" alt="image" src="https://github.com/user-attachments/assets/01fb9932-8a11-48ba-9f80-7c3348578a4b" />

We research /usr/bin/busctl on GTFOBins to identify potential methods for exploiting it to escalate privileges on the target system.

<img width="976" height="402" alt="image" src="https://github.com/user-attachments/assets/06b3237e-1f15-4e8f-bb71-82a3a511a701" />

After applying the exploit from GTFOBins, we successfully obtain a root shell, completing the final lab.

<img width="602" height="216" alt="image" src="https://github.com/user-attachments/assets/13629f97-eeca-4727-a3d8-729c2ebc136b" />

<img width="438" height="189" alt="image" src="https://github.com/user-attachments/assets/eaddc439-ed3f-4782-9322-c310797c2437" />
