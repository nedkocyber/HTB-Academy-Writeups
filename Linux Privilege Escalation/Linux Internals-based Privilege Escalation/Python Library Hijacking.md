# Python Library Hijacking

Python Library Hijacking occurs when an attacker places a malicious Python module or package in a location that Python searches before the legitimate library, causing Python to import the attacker’s code instead of the intended one.

<img width="1004" height="277" alt="image" src="https://github.com/user-attachments/assets/3ae35bf3-13c6-4e76-aa8f-3ac6f54edf4e" />

From sudo -l, we observe that the user is allowed to run mem_stats.py with elevated privileges.

<img width="489" height="383" alt="image" src="https://github.com/user-attachments/assets/1da9223b-8ce5-4d5e-8af5-0d45bb62bf64" />

We modify the mem_stats.py script to execute cat on the flag file. After running the modified script with sudo, we successfully read the flag and complete the lab.

<img width="907" height="97" alt="image" src="https://github.com/user-attachments/assets/67cc57e4-64a9-476b-a1b4-3f840336f587" />
