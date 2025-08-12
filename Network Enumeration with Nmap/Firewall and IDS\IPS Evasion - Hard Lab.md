# Firewall and IDS\IPS Evasion - Hard Lab

Now this lab is hard becasue to evade the IDS/IPS there are allot of flags that need to be used

<img width="1033" height="40" alt="image" src="https://github.com/user-attachments/assets/1045e8c0-06e7-4e96-bc10-364b60aa9021" />

After the scan if everythig went well we are going to see a service running on port 50000 tcpwrapped

<img width="1043" height="110" alt="image" src="https://github.com/user-attachments/assets/eb78c3ee-6315-42ca-a4b8-a8b271526f2a" />

Now we can try connectiong to that port with netcat and obtain the flag

<img width="597" height="132" alt="image" src="https://github.com/user-attachments/assets/4c0f074e-8d5e-431d-99e9-b437d85a30ab" />

 Attempts to connect to port 50000 on 10.129.2.47.
 Uses port 53 as the outbound port → This can bypass firewalls because DNS traffic (port 53) is often allowed through firewalls.
 Displays detailed connection information.

 # Conclusion
Overall, this lab serves as a critical foundation for anyone pursuing a career in penetration testing. The reconnaissance phase, combined with in-depth Nmap enumeration, forms the backbone of any successful penetration test. By systematically gathering information about the target and identifying potential attack vectors, the tester establishes a solid basis for the subsequent exploitation phase. Mastery of these techniques not only improves efficiency but also increases the likelihood of uncovering vulnerabilities that might otherwise remain hidden.
