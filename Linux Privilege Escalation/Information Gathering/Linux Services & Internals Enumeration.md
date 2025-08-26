# Linux Services & Internals Enumeration

ls /usr/bin | grep -E '^python3\.[0-9]+$'

ls /usr/bin → lists all files in the /usr/bin directory.
grep -E '^python3\.[0-9]+$' → uses an extended regular expression (regex) to filter only filenames that start with python3. followed by one or more digits, e.g., python3.6, python3.8, python3.11.

<img width="455" height="78" alt="image" src="https://github.com/user-attachments/assets/2fac2e26-e061-494f-b37b-fca69cc2007e" />
