# Footprinting Lab - Medium

Again we start it with an nmap scan to see all the ports and services

<img width="1039" height="844" alt="image" src="https://github.com/user-attachments/assets/87e50460-7ef5-408c-8e14-aeabe79a7211" />
<img width="1039" height="530" alt="image" src="https://github.com/user-attachments/assets/741f9965-3d15-4053-9b5e-053da7853523" />

We see that we have port 111/NFS open so we try attacking it first

<img width="506" height="124" alt="image" src="https://github.com/user-attachments/assets/4fdfe8ea-8db3-4243-8d9b-aa86645a050f" />

<img width="637" height="510" alt="image" src="https://github.com/user-attachments/assets/01f78d27-a006-4a17-96eb-fb1130514774" />

We see thta we have a bunch of tickets and we start looking for something that sticks out 

We see one that has different size from the others

<img width="854" height="154" alt="image" src="https://github.com/user-attachments/assets/a2a62f72-ed96-4d2b-a1c1-537a326cff3a" />

When we open it we find credentials 

<img width="509" height="155" alt="image" src="https://github.com/user-attachments/assets/2d63870b-3091-49ae-abfa-ee7e95f3c241" />

With the credentials now we try logging somewhere

and SMB seems to work with theese credentials

<img width="1031" height="325" alt="image" src="https://github.com/user-attachments/assets/e894becb-e23b-4017-b22e-baa3a5d35481" />

in DEVSHARE we find another pair of credentials 

<img width="1039" height="448" alt="image" src="https://github.com/user-attachments/assets/4e90227e-1c9c-41fa-b907-c66d7ad0ee07" />

Now we try logging with xfreerdp

<img width="1034" height="130" alt="image" src="https://github.com/user-attachments/assets/819a2660-b0d7-49f0-8dc6-c84d3a1c3c09" />

Very IMPORTANT RUN AS ADMINISTRATOR or its not gonna work

<img width="1036" height="816" alt="image" src="https://github.com/user-attachments/assets/a8ac9d56-6be0-47ae-94cb-085b2f3c16bb" />

<img width="904" height="689" alt="image" src="https://github.com/user-attachments/assets/c2ab8d16-a88d-406b-af85-c60614dc98e3" />

 Entering the password we found earlyer 

 And we connect to the database

<img width="694" height="454" alt="image" src="https://github.com/user-attachments/assets/71fd5003-3c54-43b6-be50-e248f4c62403" />

With a little bit of digging we find the flag/password

<img width="1042" height="792" alt="image" src="https://github.com/user-attachments/assets/1769eadd-97a1-4887-8696-4cb21328cece" />

