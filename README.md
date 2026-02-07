README.md
# My Website

This is my first static website hosted on an Ubuntu server using NGINX.  
The project contains HTML, CSS, and JavaScript files that make up the website layout and design.

## 🚀 Deployment Steps (Ubuntu + NGINX)

1. **Update and upgrade the server**
   ```bash
   sudo apt update -y && sudo apt upgrade -y 
<img width="1919" height="992" alt="Screenshot 2025-11-22 173319" src="https://github.com/user-attachments/assets/874efefe-6592-4237-8d4e-68cd808ff550" />

 
2. Install NGINX

sudo apt install nginx -y


3. Start and enable NGINX

sudo systemctl start nginx
sudo systemctl enable nginx
<img width="1435" height="695" alt="Screenshot 2025-11-22 174252" src="https://github.com/user-attachments/assets/7e09e5e8-e76a-43b0-a753-b2dc2583a631" />


4. Upload your website files
From your local machine:

scp -i "server1.pem" -r my-website/ ubuntu@<Public-IP>:/var/www/html/
<img width="1918" height="1000" alt="Screenshot 2025-11-22 184905" src="https://github.com/user-attachments/assets/b66c5300-90c0-4310-8f0b-6bd39082ca4a" />


5. Set correct permissions

sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html
<img width="787" height="439" alt="Screenshot 2025-11-22 185306" src="https://github.com/user-attachments/assets/a5308db0-c173-409f-bc79-6e5a326eafb4" />


6. Restart NGINX

sudo systemctl restart nginx
<img src="Screenshot 2025-11-22 185306.png

🌐 Access Website

Open in browser:
<img width="1919" height="1079" alt="Screenshot 2025-11-22 185412" src="https://github.com/user-attachments/assets/c0f91476-9cc2-4276-9602-5aefb8aaec70" />


http://<Public-IP>

📁 Folder Structure
my-website/
│── index.html
│── styles.css
│── script.js
└── assets/

✨ Notes

Replace <Public-IP> with your EC2 instance’s public IPv4 address.

Ensure port 80 is allowed in your EC2 security group.
