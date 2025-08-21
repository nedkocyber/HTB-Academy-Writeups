# Value Fuzzing POST

When navigating to the IP in the browser, we are presented with a message, but we proceed directly to fuzzing the web application to discover hidden paths or files.

<img width="1047" height="287" alt="image" src="https://github.com/user-attachments/assets/6c496c56-597f-4c7f-885d-44dd2ac8ecee" />

We fuzz the id parameter via a POST request to identify valid inputs, filtering out irrelevant responses based on size using -fs 768.

<img width="882" height="321" alt="image" src="https://github.com/user-attachments/assets/04606335-116e-40ed-92e2-5a21afe03b01" />

This curl command sends a POST request with id=73 to test the server’s response, using the correct content type for form submissions. While not strictly necessary for solving the lab, it's a good exercise for practicing manual request crafting with curl.

<img width="788" height="222" alt="image" src="https://github.com/user-attachments/assets/4d1cac03-5855-4416-847c-271f78b11b07" />

curl `http://admin.academy.htb:31200/admin/admin.php` \
-X POST \
-d 'id=73' \
-H 'Content-Type: application/x-www-form-urlencoded'
