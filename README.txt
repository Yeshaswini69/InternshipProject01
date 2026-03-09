# AWS EC2 Node.js Web Application with S3 Image Gallery

## Project Overview
This project demonstrates how to deploy a Node.js web application on an AWS EC2 instance and integrate it with Amazon S3 for hosting images.

The application displays a completion page with a personalized message and an image gallery where images are fetched from an Amazon S3 bucket.

This project showcases basic cloud deployment and integration between compute and storage services in AWS.

## Architecture
User Browser → EC2 Instance (Node.js + Express) → Amazon S3 (Image Storage)

## Technologies Used
- Node.js
- Express.js
- Amazon EC2
- Amazon S3
- Linux (Ubuntu)

### Amazon S3
- Created an S3 bucket
- Uploaded images to the bucket
- Enabled public access to images
- Used public URLs to display images in the application
## S3 Image Integration
Images are stored in an Amazon S3 bucket and accessed using public URLs.
These URLs are embedded in the completion.html file to display an image gallery.

### Secure Access to EC2

Instead of using SSH keys, the EC2 instance was accessed securely using AWS Systems Manager Session Manager.

Steps followed:

1. Created an IAM role with the required Systems Manager permissions.
2. Attached the IAM role to the EC2 instance.
3. Connected to the instance using AWS Systems Manager Session Manager from the AWS Console.
4. Managed the server directly through the browser-based terminal.

---
1. Connected to the EC2 instance using AWS Systems Manager Session Manager.
2. Created application files using the vi editor.
Create server file:
vi app.js
Create webpage file:
vi completion.html
3. Installed Node.js and verified installation:
node -v
npm -v
4. Ran the application:
node app.js
5. Accessed the application in a browser using:
http://<EC2-PUBLIC-IP>

## Learning Outcomes

Through this project, I gained hands-on experience with several core AWS and cloud deployment concepts:

- Learned how to launch and configure an EC2 instance using Ubuntu.
- Understood how to securely access an EC2 instance using AWS Systems Manager Session Manager with an IAM role instead of SSH keys.
- Installed and verified Node.js and npm on a Linux server environment.
- Built and ran a simple web server using Node.js and Express.
- Deployed a web application on a cloud virtual machine.
- Created and configured an Amazon S3 bucket to store static images.
- Integrated S3 public image URLs into a web application.
- Configured EC2 security groups to allow HTTP traffic so the application could be accessed through a browser.
- Gained practical experience working with Linux commands and the vi editor to create and manage application files.

---

## Author
Yeshaswini  
Cloud Engineer

