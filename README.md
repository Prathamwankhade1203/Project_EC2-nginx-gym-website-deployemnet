README.md
# My Website

This is my first static website hosted on an Ubuntu server using NGINX.  
The project contains HTML, CSS, and JavaScript files that make up the website layout and design.

## 🚀 Deployment Steps (Ubuntu + NGINX)

1. **Update and upgrade the server**
   ```bash
   sudo apt update -y && sudo apt upgrade -y
<img src="Screenshot 2025-11-22 174010.png>
 
2. Install NGINX

sudo apt install nginx -y

<img src=

3. Start and enable NGINX

sudo systemctl start nginx
sudo systemctl enable nginx
<img src="Screenshot 2025-11-22 183327.png

4. Upload your website files
From your local machine:

scp -i "server1.pem" -r my-website/ ubuntu@<Public-IP>:/var/www/html/


5. Set correct permissions

sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html


6. Restart NGINX

sudo systemctl restart nginx
<img src="Screenshot 2025-11-22 185306.png

🌐 Access Website

Open in browser:
<<img src="Screenshot 2025-11-22 185346.png>

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