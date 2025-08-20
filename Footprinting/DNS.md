# DNS

<img width="1046" height="339" alt="image" src="https://github.com/user-attachments/assets/094104ac-9a8e-4d48-8a38-08bfc41c9bcc" />

First, we use the dig command to discover the FQDN associated with the inlanefreight.htb domain.

<img width="1046" height="332" alt="image" src="https://github.com/user-attachments/assets/a700ed8a-8ba0-408c-83ed-1577a539c620" />

To determine whether a DNS zone transfer was possible, we used the dig command targeting the authoritative DNS server for the domain. By specifying the domain, the name server (@IP) and using the AXFR query type, we were able to successfully transfer the DNS zone.

<img width="1034" height="417" alt="image" src="https://github.com/user-attachments/assets/7fd2fb60-9b8d-4308-840c-0a9e62357bb6" />

Based on the information gathered and the screenshot provided, we identified the IP address of the domain controller dc1 as 10.129.34.16.

For some reason, I was unable to perform the task on my Kali machine, so I switched to the built-in VM on HTB. Using the command there, I successfully identified the FQDN of the host with an IP address ending in .203.

dnsenum --dnsserver 10.129.129.105 --enum -p 0 -s 0 -o subdomains.txt -f /opt/useful/SecLists/Discovery/DNS/fierce-hostlist.txt dev.inlanefreight.htb

<img width="1036" height="622" alt="image" src="https://github.com/user-attachments/assets/c223c2aa-ec13-494d-9c63-d23cfc0b1f51" />
