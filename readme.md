# README: EC2 Instance Setup and AMI Creation

## Overview
This document provides a step-by-step guide on how to create an Amazon EC2 instance, configure it by writing a file and installing Nginx, create an AMI image from the configured instance, and launch a new EC2 instance using the AMI.

## Steps Performed

### 1. **Launch an EC2 Instance**
- Created an Amazon EC2 instance.
- Chose an appropriate Amazon Machine Image (AMI) and instance type. I used Ubuntu here.
- Configured security groups and key pairs as needed.

### 2. **Write a File in the EC2 Instance**
- Connected to the instance using Putty.
- Update packages

  sudo apt update
  
- Created a file in the instance:
  
  vi sample.txt

### 3. **Install Nginx**
- Updated the package repository:

  sudo apt update -y

- Installed Nginx:
 
  sudo apt install -y nginx   # Ubuntu
  
- Started and enabled the Nginx service:

  sudo systemctl start nginx
  sudo systemctl enable nginx
  
- Verified Nginx installation by accessing the instance's public IP in a web browser.

- Commands used:



### 4. **Create an AMI Image**
- Created an AMI image from the configured EC2 instance via the AWS Management Console or CLI:
  

### 5. **Launch a New EC2 Instance Using the AMI**
- Created a new EC2 instance from the AMI using the AWS Console or CLI:
  

- Verified that the file and Nginx installation persisted in the new instance.

## Verification
- SSH into the new instance and check for the created file:
   
   ls
  
- Verify Nginx is running:

  sudo systemctl status nginx
  

## Conclusion
By following these steps, we successfully created a customized EC2 instance, converted it into an AMI, and used that AMI to launch a new EC2 instance with the same configurations.

