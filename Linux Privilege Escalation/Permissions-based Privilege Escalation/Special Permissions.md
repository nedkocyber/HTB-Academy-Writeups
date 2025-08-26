# Special Permissions

SetUID: When a file (usually an executable) has this bit set, it runs with the permissions of its owner, typically root, even if executed by a regular user.
➤ This can grant elevated privileges beyond normal user rights, which is why it’s considered risky.

SetGID: Works similarly, but applies to the group instead of the user.
➤ The process executes with the group privileges of the file’s group, potentially allowing access to restricted resources.

<img width="1048" height="687" alt="image" src="https://github.com/user-attachments/assets/a21439ad-f5a1-4b9f-8dbb-a3e9e14806cc" />

<img width="995" height="74" alt="image" src="https://github.com/user-attachments/assets/3f38f16f-ed59-4512-9d35-f0d01381acf5" />
