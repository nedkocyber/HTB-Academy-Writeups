# Containers

We are a part of the lxd

<img width="938" height="47" alt="image" src="https://github.com/user-attachments/assets/e8837f81-cb48-4997-bdf1-5c7c9eecd37a" />

We import an Alpine Linux image into LXC and assign it the alias ubuntuteam

Upon successful import, LXC confirms with a message and the image fingerprint.

<img width="938" height="47" alt="Screenshot 2025-08-27 114323" src="https://github.com/user-attachments/assets/fa67a6ff-96b4-4077-95b5-607f1f7d8d83" />

We initialize a privileged Alpine container named privesc from the ubuntuteam image (security.privileged=true) and mount the host’s root filesystem inside it (/mnt/root). After starting the container and accessing its shell, we immediately have full root privileges on the host (uid=0, gid=0), enabling unrestricted access and modification of the host system.

<img width="1012" height="220" alt="Screenshot 2025-08-27 114148" src="https://github.com/user-attachments/assets/a7b75ff8-2045-49d8-98ba-17f55dfff759" />

<img width="352" height="64" alt="image" src="https://github.com/user-attachments/assets/97c0a1b9-5896-48a6-9807-608fc33222ff" />
