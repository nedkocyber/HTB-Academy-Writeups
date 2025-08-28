# Sudo

From running sudo -l, we can see that the user is allowed to execute /bin/ncdu with elevated privileges.

<img width="1043" height="146" alt="image" src="https://github.com/user-attachments/assets/67b4ade8-7381-4eef-b4cb-31b42a45af3e" />

This command runs /bin/ncdu as root (UID -1), giving us access to the /root directory

<img width="595" height="27" alt="image" src="https://github.com/user-attachments/assets/1eee94af-d5ad-44e1-9ce4-93f9510d5466" />

Now, by using ?, we can view all the available options and commands within ncdu

<img width="675" height="349" alt="image" src="https://github.com/user-attachments/assets/15af6c65-5469-43bf-a3bb-d56512d53fb0" />

Once we have a shell, we can simply retrieve the flag

<img width="1032" height="227" alt="image" src="https://github.com/user-attachments/assets/ca4fbd9f-95fb-45b7-a02e-9ea7c21450ec" />

<img width="286" height="49" alt="image" src="https://github.com/user-attachments/assets/50849add-69aa-4da0-acfd-77af0a0bf7ce" />
