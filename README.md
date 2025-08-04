# Networking Assignment
## NGINX on EC2 with custom domain

This assignment demonstrates the deployment of a basic web server using an AWS EC2 instance running NGINX on port 80. The project includes configuring an A record in either Cloudflare to point a custom domain (e.g., sarmad.sarmadcloud.work) to the public IP address of the EC2 instance. The goal is to make the NGINX welcome page accessible via the domain, showcasing end-to-end connectivity from DNS configuration to web server deployment.

## Process

### 1. Buying and configuring domain
First I went on to CloudFlare and bought a domain **sarmadcloud.work**, CloudFlare allowed me to create an **A** record to link it to my EC2 instance (using the public IP address) that would have NGINX running on port 80.

### 2. Create EC2 instance
