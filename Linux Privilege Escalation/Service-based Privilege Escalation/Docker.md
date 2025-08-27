# Docker

We see that we are a member of the group docker

<img width="963" height="48" alt="image" src="https://github.com/user-attachments/assets/88ffbf98-c1fa-4f61-b1c7-56c389c42e0e" />

If a user has access to docker.sock or is part of the Docker group, they can start a shell as root inside a container because the host filesystem is effectively accessible through the mounted Docker container. This provides a straightforward privilege escalation vector from a standard user to root.

<img width="915" height="69" alt="image" src="https://github.com/user-attachments/assets/b83fcd0b-f32c-42d6-a6be-580b46eedeb2" />

<img width="468" height="44" alt="image" src="https://github.com/user-attachments/assets/1aee184a-5dea-476b-a064-796d2de7cd8e" />
