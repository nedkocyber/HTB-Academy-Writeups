# Shared Libraries

<img width="1374" height="119" alt="image" src="https://github.com/user-attachments/assets/f77e44d8-9457-403f-b52d-fa8cfbbacd21" />

init() → This is an ELF init hook, automatically called when the shared library is loaded, before main() of the target program.
unsetenv("LD_PRELOAD") → Removes the LD_PRELOAD environment variable to prevent it from affecting subsequent shells or causing reload loops/glitches.
setgid(0); setuid(0); → Sets the GID and UID to 0 (root) for the current process. Since the process is already running via sudo, this ensures full root privileges for the next command.
system("/bin/bash"); → Launches a root shell in the current terminal.

<img width="423" height="292" alt="image" src="https://github.com/user-attachments/assets/a82c76c6-f67f-4b13-95a4-7a9f229bb60d" />

gcc -fPIC -shared -o /tmp/root.so exploit.c -nostartfiles

-fPIC → Generates position-independent code, required for shared libraries (.so)
-shared → Produces a shared library instead of an executable.
-o /tmp/root.so → Specifies the output file name and location.
-nostartfiles → Omits standard startup files; keeps the .so clean. Not strictly necessary, but often used in exploitation to avoid extra initialization code.

<img width="1390" height="38" alt="image" src="https://github.com/user-attachments/assets/9a30d176-2235-44f0-ba7f-87f841a637d9" />

<img width="896" height="72" alt="image" src="https://github.com/user-attachments/assets/7ee8c35a-e909-4bf2-aecf-e0a4a010319d" />

<img width="515" height="47" alt="image" src="https://github.com/user-attachments/assets/1b4a9684-f437-473c-8787-6d149160a6ba" />
