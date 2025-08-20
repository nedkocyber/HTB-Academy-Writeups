# Footprinting Lab - Hard

Important is to do a full port scan on every target to see everything possible ( i know i didint show it past labs but its important trust me :D)

nmap -p- -T5 10.129.202.20 -Pn  whith this command we find all the ports that are running

<img width="1026" height="521" alt="Screenshot 2025-08-12 162725" src="https://github.com/user-attachments/assets/de0fbc4a-7666-4c5b-ba73-e4c084790d7a" />

<img width="1042" height="85" alt="image" src="https://github.com/user-attachments/assets/461b0cec-a622-4350-aa06-9e9ddf2ed314" />

With this command we find comunity string 

<img width="880" height="145" alt="image" src="https://github.com/user-attachments/assets/7f17752f-649c-40c2-b863-083047c361aa" />

Here we login with what we found

<img width="1050" height="91" alt="image" src="https://github.com/user-attachments/assets/cdd9cf8c-158d-48bc-a657-ffc7601f5d45" />

Here i can demonstrate all the ways u can possibly get it wrong like me and waste 20 minutes of your lofe for a singe charecter

<img width="989" height="276" alt="image" src="https://github.com/user-attachments/assets/ce6b9dbf-ba28-43ce-b441-d587588246ae" />

<img width="545" height="216" alt="image" src="https://github.com/user-attachments/assets/bb215ddd-23ea-4d93-95cc-be925a8a53e3" />

Here we find a private key

<img width="874" height="739" alt="image" src="https://github.com/user-attachments/assets/e9c9e16a-ba7a-40bb-9cc4-23c88ae88292" />

we login with the key we found and start digging 

<img width="800" height="82" alt="image" src="https://github.com/user-attachments/assets/110cb3da-1f41-42bb-93d9-bdab5ea228cf" />

We find some inturesting running services here

<img width="1340" height="238" alt="image" src="https://github.com/user-attachments/assets/f8ddf8b0-4a94-4c30-8714-8f043350deb3" />

The one we are inturested is mysql

<img width="460" height="879" alt="image" src="https://github.com/user-attachments/assets/a3606cb0-8ce9-45a8-a860-601d7019bf78" />

After little bit of searching we find the flag

<img width="903" height="748" alt="image" src="https://github.com/user-attachments/assets/b0613f49-fbb3-402a-9bc9-154e256f172e" />






