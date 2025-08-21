# IMAP/POP3

IMAP (Internet Message Access Protocol)

Allows direct access to emails on the server without downloading them locally.
Emails remain on the server until explicitly deleted.
Supports folders and hierarchical structure, syncing across multiple devices (mobile, desktop, etc.).
Operates on port 143 (unencrypted) or port 993 (with TLS/SSL encryption).
Without encryption, username and password are transmitted in plain text!
Uses commands like LOGIN, SELECT, FETCH, LOGOUT, etc.

POP3 (Post Office Protocol v3)

Older and simpler protocol – downloads emails locally and removes them from the server.
Does not support folders or synchronization across devices.
Runs on port 110 (unencrypted) or port 995 (with TLS/SSL).
Suitable for single-device use without needing access from multiple clients.


<img width="1045" height="442" alt="image" src="https://github.com/user-attachments/assets/959a6a25-4d2c-4ce0-b104-ebc427b0b8af" />
<img width="1034" height="117" alt="image" src="https://github.com/user-attachments/assets/ff4d0e8c-9df2-49b5-9021-e9fbc5da7a2e" />

Using openssl s_client -connect 10.129.240.178:pop3s and openssl s_client -connect 10.129.240.178:imaps, we establish secure connections to both the POP3S and IMAPS services respectively.

<img width="1034" height="142" alt="image" src="https://github.com/user-attachments/assets/b76b8fe7-a6f5-4af2-99f3-09c4da13b726" />

<img width="1036" height="38" alt="image" src="https://github.com/user-attachments/assets/d80c7c6c-7870-4d98-83c1-499f6c45d11e" />

<img width="327" height="221" alt="image" src="https://github.com/user-attachments/assets/2fb501ee-2ed5-4c07-a632-75de69530c1d" />

Command	Description
USER username	Identifies the user.
PASS password	Authenticates the user with the provided password.
STAT	Requests the number of messages and their total size on the server.
LIST	Lists all messages with their corresponding sizes.
RETR id	Retrieves the email with the specified ID.
DELE id	Deletes the email with the specified ID from the server.
CAPA	Displays the capabilities supported by the server.
RSET	Resets the session, undeleting any messages marked for deletion.
QUIT	Ends the session and closes the connection with the POP3 server.

We used this set of POP3 commands to interact with the mail server and successfully complete the lab.

<img width="1044" height="53" alt="image" src="https://github.com/user-attachments/assets/f48c4277-0da3-446f-80ba-c759ae455a64" />

Here we Login with the credentials robin robin

<img width="608" height="147" alt="image" src="https://github.com/user-attachments/assets/4c51a8f2-cbae-4e0e-ad02-874a2b0095df" />

We list the contents of the directory

<img width="1053" height="37" alt="image" src="https://github.com/user-attachments/assets/6c94d2fd-00c0-439e-8620-4f57964085de" />

<img width="1045" height="587" alt="image" src="https://github.com/user-attachments/assets/a3505d22-3b5c-48f3-9fd0-230942bb9708" />


