# Travel-Memory-Application-Deployment

Overview
This document provides a comprehensive guide to deploying the Travel Memory MERN stack application on AWS EC2 with load balancing and custom domain configuration.

# Step-by-Step Deploymen

✅ 	Launch EC2 Instance:
o	Log in to AWS Console

o	Navigate to EC2 service in Oregon region (us-west-2)

o	Click "Launch Instance"

o	Name: TravelMemory-Production

o	AMI: Ubuntu 22.04 LTS

o	Instance type: t2.micro (free tier eligible)

o	Key pair: Create new or use existing (download .pem file)

o	Network settings: Allow HTTP (80), HTTPS (443), and custom TCP (3000, 5000) traffic

o	Launch instance

![image](https://github.com/user-attachments/assets/3d815128-4c30-4d0b-9228-91aadbd67f50)


✅ 	Connect to Instance:
![image](https://github.com/user-attachments/assets/559d9591-1ceb-4671-baff-2ee3b83ad88d)

✅ 	Update System Packages:
   
     ![image](https://github.com/user-attachments/assets/896e7217-d46d-465c-a28d-42c2720ef6a1)

*********************************************************************************************************************************************************************
# Application Setup

✅  Install Dependencies:
 ![image](https://github.com/user-attachments/assets/f22fab3b-049f-4a6a-99a5-f17025e315a5)

✅  Install Application:
sudo apt install node
sudo apt install npm
sudo apt install nginx

✅ Check Versions:

 ![image](https://github.com/user-attachments/assets/4bcf024e-7673-4b2f-b2d0-5803ccb2352d)

✅  Clone Repository:
![image](https://github.com/user-attachments/assets/d715b5bb-9e23-43f5-bbeb-fbcd7342bd39)


*********************************************************************************************************************************************************************

# Backend Configuration

✅  Navigate to the Backend Directory:

 ![image](https://github.com/user-attachments/assets/b91e4594-43bc-41b2-9d8e-0844e30d4cfb)

✅  Install Dependencies:
 ![image](https://github.com/user-attachments/assets/bd5c2fb6-8c7a-4f95-9811-18344c3f3b36)

✅  Configure Environment Variables:
  ![image](https://github.com/user-attachments/assets/2f391f5e-ca45-4f61-8fe1-fa6e21ca6502)

✅  Test Backend:
 ![image](https://github.com/user-attachments/assets/1b3b8fea-67ca-4ff6-a7df-1b69dfcc7102)

 ![image](https://github.com/user-attachments/assets/7da1c3fa-0b64-4cdd-a985-5f6e35202fd9)

✅  PM2 Setup (for process management):
 ![image](https://github.com/user-attachments/assets/67e0d754-5706-486c-a40e-85d2b50d7e67)

 ![image](https://github.com/user-attachments/assets/c1218c31-1c24-4d25-866a-93c721cc14bd)

*********************************************************************************************************************************************************************
# Frontend Configuration

✅ Navigate to Frontend Directory:
 ![image](https://github.com/user-attachments/assets/b03f2f46-de43-4497-90da-73afc45e1dce)


✅ Install Dependencies:
 ![image](https://github.com/user-attachments/assets/0aed1c93-eba0-4ea2-b6af-fd2e620e5488)

 ![image](https://github.com/user-attachments/assets/acea448c-84aa-4e5b-aac7-d184bf5ff7f4)


✅ Update API Endpoints:
 ![image](https://github.com/user-attachments/assets/f19fa8c7-15e7-4628-bf38-1b74da9eb62a)


✅ Build Production Version:
 ![image](https://github.com/user-attachments/assets/718c3e8b-e658-4202-82e2-2c8b9a3e77ee)


✅ Serve Frontend with PM2:
 ![image](https://github.com/user-attachments/assets/89a1a9a5-df4a-4ec6-99be-e5e636839bb6)

 ![image](https://github.com/user-attachments/assets/73a32b9e-22c7-43fe-ad2f-7a0c35694b88)

 ![image](https://github.com/user-attachments/assets/5136f6a6-5fdd-450d-b7e8-39bde51899b7)


*********************************************************************************************************************************************************************
# Nginx Configuration

✅ Configure Nginx as a Reverse Proxy:
 ![image](https://github.com/user-attachments/assets/3ac5b95b-3684-419b-889d-052485fa6aa2)



✅ Enable Configuration:
 ![image](https://github.com/user-attachments/assets/33e029e3-58a3-4a4c-a7e6-0f297aacbcfb)

 ![image](https://github.com/user-attachments/assets/c6215501-2476-4788-a48b-703c3b6a0b73)


*********************************************************************************************************************************************************************
# Load Balancer Setup

✅ Create Additional EC2 Instances:
 Created 2 EC2 istances with same configurations

✅ Create Application Load Balancer:
 Created a new load balancer with the newly created target group


✅ Update Nginx Configuration:
 Updated Nginx configurations


*********************************************************************************************************************************************************************

# Domain Configuration with Cloudflare

✅ Add Domain to Cloudflare & Configure DNS Records:: 
 ![image](https://github.com/user-attachments/assets/69ba075f-6384-46c9-89dd-8c56f778d3cd)


✅ SSL Configuration:
 Updated

*********************************************************************************************************************************************************************
# Verification

✅ Check Application Status:
 ![image](https://github.com/user-attachments/assets/3e80927d-4017-4761-a32b-fcf81be96544)


✅ Access Application:

http://swetabhsonal.com

http://172-31-42-250:

http://swetabh-tmad-alb-824108635.us-west-2.elb.amazonaws.com

 ![image](https://github.com/user-attachments/assets/45efca0a-60f3-43a8-9f7c-ac87b754d717)

*********************************************************************************************************************************************************************

## Thank You ##


