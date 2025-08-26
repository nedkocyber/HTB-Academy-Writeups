# Capabilities

Capabilities are 

find /usr/bin /usr/sbin /usr/local/bin /usr/local/sbin -type f -exec getcap {} \;

find /usr/bin /usr/sbin /usr/local/bin /usr/local/sbin → searches in common binary directories.
-type f → limits the search to regular files (excludes directories).
-exec getcap {} \; → runs getcap on each file found to list any Linux capabilities assigned to it.

<img width="1044" height="101" alt="image" src="https://github.com/user-attachments/assets/52fd49d9-20f4-4aa4-a6da-00527328ac80" />

We notice that we have full privileges on vim.basic. Using this, we can remove the root password from /etc/passwd.

<img width="574" height="99" alt="image" src="https://github.com/user-attachments/assets/e3c03d54-c9a4-47c1-af2d-c20006016ac8" />

We have successfully removed the root password, allowing us to log in as root without authentication and gain full system control.

<img width="1034" height="60" alt="image" src="https://github.com/user-attachments/assets/b60e23c5-814d-408e-938f-bee6004e449c" />

<img width="833" height="453" alt="image" src="https://github.com/user-attachments/assets/46dfcf49-d22d-46ba-820d-75e2746cbd06" />
