# Credential Hunting

find / ! -path "*/proc/*" -iname "*php*" -type f 2>/dev/null

find / → starts searching from the root directory /.
! -path "*/proc/*" → excludes any paths under /proc to avoid unnecessary or virtual filesystem entries.
-iname "*php*" → searches for files whose names contain php, case-insensitive.
-type f → limits results to regular files (ignores directories, links, etc.).
2>/dev/null → suppresses error messages (like permission denied) by redirecting them to /dev/null.

<img width="529" height="14" alt="image" src="https://github.com/user-attachments/assets/8effdbdf-6d9a-4808-8cb1-217bab146754" />


<img width="412" height="236" alt="image" src="https://github.com/user-attachments/assets/5d7b4de2-49a7-4a4e-8bd6-87ffb6d13537" />

There’s a WordPress configuration file (/wp-config.php) on the system. Inside, we find the database username and password

<img width="537" height="43" alt="image" src="https://github.com/user-attachments/assets/d6e474f4-dfee-45a6-8518-d434cae538dd" />
