# Travel-Memory-Application-Deployment

Overview
This document provides a comprehensive guide to deploying the Travel Memory MERN stack application on AWS EC2 with load balancing and custom domain configuration.

# Step-by-Step Deploymen

1.	Launch EC2 Instance:
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


2.	Connect to Instance:
![image](https://github.com/user-attachments/assets/559d9591-1ceb-4671-baff-2ee3b83ad88d)

3.	Update System Packages:
   
     ![image](https://github.com/user-attachments/assets/896e7217-d46d-465c-a28d-42c2720ef6a1)

*********************************************************************************************************************************************************************
# Application Setup







*********************************************************************************************************************************************************************



