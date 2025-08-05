# Networking Assignment
## NGINX on EC2 with custom domain

This assignment demonstrates the deployment of a basic web server using an AWS EC2 instance running NGINX on port 80. The project includes configuring an A record in either Cloudflare to point a custom domain (e.g., sarmad.sarmadcloud.work) to the public IP address of the EC2 instance. The goal is to make the NGINX welcome page accessible via the domain, showcasing end-to-end connectivity from DNS configuration to web server deployment.

## Process

### 1. Buying and configuring domain
First I went on to CloudFlare and bought a domain **sarmadcloud.work**, CloudFlare allowed me to create an **A** record to link it to my EC2 instance (using the public IP address) that would have NGINX running on port 80.

<img width="1265" height="165" alt="image" src="https://github.com/user-attachments/assets/a7c4f163-1514-427b-b2b3-1576f8f2ab00" />


### 2. Create EC2 instance
This was then followed up by creating an EC2 instance via AWS and because we want to connect via port 80 edit the security details to contain that of port range 80

<img width="1341" height="317" alt="image" src="https://github.com/user-attachments/assets/7410e5d5-1a4c-4ba5-aed0-9995c75e0a49" />


### 3. Install NGINX
After SSH'ing into the EC2 instance, I then installed NGINX on the instance using the following commands:
'''
sudo apt update
sudo apt install nginx
'''
The first command updates everything to the latest version, the second command installs nginx

<img width="994" height="722" alt="image" src="https://github.com/user-attachments/assets/eec5f601-06cb-4c43-92cc-0ca123f7f28c" />

### 4. Testing configuration
Finally we can test that everything is working in order, by searching the domain (sarmad.sarmadcloud.work) instead of the public IP address.

<img width="1306" height="518" alt="image" src="https://github.com/user-attachments/assets/b4486832-a254-4a3b-a344-fffa4e5e523e" />

### 5. Confirm IP address is linked domain
We can then use the nslookup tool to confirm that our domain is associated with the IP address of the server

<img width="369" height="146" alt="image" src="https://github.com/user-attachments/assets/01442dab-3cab-4115-b129-7de32e6f5582" />





