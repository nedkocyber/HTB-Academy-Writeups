# SMTP

What is SMTP (Simple Mail Transfer Protocol)?

SMTP is the standard protocol for sending emails over the Internet. It defines how email messages are transferred from one server (point A) to another (point B). It is the core mechanism used by most email systems to deliver outgoing messages.

<img width="1048" height="321" alt="image" src="https://github.com/user-attachments/assets/e0526d2f-6b4d-4fc5-a9c2-a5441caae673" />

After scanning the target, we identified that SMTP is running on port 25 and appears to be misconfigured or vulnerable to exploitation.

Using msfvenom, we generated a custom payload and exploited the vulnerable service, gaining access without encountering any obstacles.

<img width="1045" height="654" alt="image" src="https://github.com/user-attachments/assets/693824b1-1f94-4b90-adaa-cbb553c3d66f" />

