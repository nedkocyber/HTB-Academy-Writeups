# Miscellaneous Techniques

At this stage, we notice that the no_root_squash service is enabled on the target, which makes it easily exploitable.

<img width="1037" height="296" alt="image" src="https://github.com/user-attachments/assets/e32ad825-ec44-4656-830b-f626542173b9" 
  />

We start by creating a local directory and mounting it to a folder on the target system. Then, using sudo, we create a shell.c file in the mounted directory with the provided code, compile it so it becomes visible on the target, and adjust its permissions and ownership.

<img width="933" height="427" alt="image" src="https://github.com/user-attachments/assets/44539c27-e5ab-4019-9093-cf7fddad034e" />
<img width="964" height="384" alt="image" src="https://github.com/user-attachments/assets/d54ae1bd-2461-49af-859c-238947110484" />

Executing the binary grants us a root shell on the target, allowing us to access the flag.

<img width="608" height="123" alt="image" src="https://github.com/user-attachments/assets/2822e2cf-e3bf-4ac1-9bdb-957655dd6e54" />
