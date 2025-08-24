# Knowledge Check

 We performed a port scan to identify the open ports and exposed services on the target machine.

 <img width="1036" height="543" alt="image" src="https://github.com/user-attachments/assets/ffea180d-ca40-45c7-8fbb-8ea033bc248a" />

"Following the port scan, we conducted a directory enumeration to identify potential entry points within the accessible web services.

<img width="1044" height="570" alt="Screenshot 2025-08-24 165820" src="https://github.com/user-attachments/assets/22011d10-f615-41a1-ab61-1ba3f37d924e" />

"Following the port scan, we conducted a directory enumeration to identify potential entry points within the accessible web services.


Initially, we were unable to access gettingstarted.htb, so we added the corresponding IP address and domain name to the /etc/hosts file using sudo nano /etc/hosts.

<img width="1219" height="531" alt="image" src="https://github.com/user-attachments/assets/68090da2-7c6a-4a39-852e-ee75a1605044" />

Since no valuable information was identified initially, we revisited the results of the directory scan. There, we discovered a /data directory containing an XML file with a hashed password.

<img width="882" height="495" alt="image" src="https://github.com/user-attachments/assets/eb8129ec-f4eb-4eac-b42c-d6de1441c8c3" />

Using CrackStation, we successfully cracked the hashed password, revealing the plaintext value admin. We then attempted to log in using these credentials.

<img width="993" height="300" alt="image" src="https://github.com/user-attachments/assets/5f8bb73e-05e4-4218-b6af-a85d45390bbd" />

We navigated back to http://gettingstarted/admin and successfully logged in using the credentials admin:admin.

<img width="1237" height="407" alt="image" src="https://github.com/user-attachments/assets/07cad670-544b-4d2f-bd7e-06a2719abcca" />

We identified the version of the GetSimple CMS 

<img width="885" height="152" alt="image" src="https://github.com/user-attachments/assets/b5b1636b-bff3-46be-a438-7d705ce17105" />

We searched for the detected version of GetSimple CMS in msfconsole and confirmed that it is vulnerable.

<img width="1041" height="135" alt="image" src="https://github.com/user-attachments/assets/7a0b677b-e96d-457c-9aa9-936596b81b76" />

Setting up the exploit.

<img width="1043" height="923" alt="image" src="https://github.com/user-attachments/assets/7b74d23b-632d-47ff-8c25-f6b00523d990" />

Now having a reverse shell we capture the user.txt flag

<img width="1000" height="718" alt="image" src="https://github.com/user-attachments/assets/fb41300a-86f6-4d8d-bcc0-88be429cc618" />

We initiated an interactive shell session using the shell command within Metasploit.

<img width="1030" height="159" alt="image" src="https://github.com/user-attachments/assets/da626fdf-4094-4fae-b13e-d0670f825349" />

We identified that the current user can execute /usr/bin/php with sudo privileges and no password. Leveraging this, we used a PHP-based privilege escalation technique from GTFOBins to escalate to root.

<img width="1023" height="207" alt="image" src="https://github.com/user-attachments/assets/5172ed77-b763-4966-903a-8337e9a24162" />

By copying and executing these two commands, we obtained a root shell, captured the root flag, and successfully completed the lab.

<img width="346" height="220" alt="image" src="https://github.com/user-attachments/assets/b9b99e79-7bf1-4767-be0e-1868ab3ad842" />

<img width="387" height="177" alt="image" src="https://github.com/user-attachments/assets/f627cbaa-eaa3-41e1-b933-60bff7eef516" />
