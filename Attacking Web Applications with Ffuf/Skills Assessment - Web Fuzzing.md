# Skills Assessment - Web Fuzzing

We begin by adding the target IP address to our /etc/hosts file to map the domain locally and ensure proper name resolution during testing.

<img width="706" height="267" alt="image" src="https://github.com/user-attachments/assets/8d0675a2-d3d0-4c45-a2e3-e5802e9ca408" />

Then, we perform a subdomain enumeration scan to identify any accessible subdomains that may expand the attack surface.

<img width="1048" height="403" alt="image" src="https://github.com/user-attachments/assets/ac9f8a89-b89a-4272-8e0e-8a7c58f537e0" />

Afterward, we perform a scan for possible file extensions on each of the discovered subdomains.

<img width="982" height="39" alt="image" src="https://github.com/user-attachments/assets/54beff46-7bed-4509-8503-5c76602bb6f6" />
<img width="697" height="60" alt="image" src="https://github.com/user-attachments/assets/7656a407-6266-4010-8fb2-28b47b2a31d1" />

ffuf -w /usr/share/seclists/Discovery/Web-Content/web-extensions.txt:FUZZ -u http://faculty.academy.htb:52248/indexFUZZ

Now, we proceed to scan for subdirectories to discover hidden files or directories.

feroxbuster -u http://faculty.academy.htb:52248/ -w /usr/share/wordlists/SecLists/Discovery/Web-Content/directory-list-2.3-medium.txt -x php,phps,php7

<img width="1037" height="501" alt="image" src="https://github.com/user-attachments/assets/180de198-9778-4d82-8a9b-cfef1fa0c260" />

We discover this hidden subdirectory, after which we proceed to fuzz the parameters and payloads.

<img width="1044" height="749" alt="image" src="https://github.com/user-attachments/assets/cb02890a-6bb7-4de0-902f-6ed3dfb6b806" />

We get two matches, and now, using an appropriate wordlist, we will fuzz for parameters like user and username to check if any of them are accepted by the server.

<img width="1044" height="82" alt="image" src="https://github.com/user-attachments/assets/d1207852-ef54-4aa4-a9d7-fe0ab7afce79" />
<img width="304" height="40" alt="image" src="https://github.com/user-attachments/assets/d1a57244-b6e5-440e-bba7-26e05dbf9548" />

Here, I demonstrate both the correct and incorrect ways to execute the command in order to successfully obtain the flag for the task.

<img width="1019" height="178" alt="image" src="https://github.com/user-attachments/assets/fa055372-df9e-4cce-8451-25bd9f4c4a17" />

