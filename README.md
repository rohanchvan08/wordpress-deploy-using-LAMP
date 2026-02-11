# Wordpress depoly using LAMP 

## :round_pushpin: Introduction ##
WordPress is a popular open-source Content Management System (CMS) used to create dynamic websites and blogs. It is written in PHP and uses MySQL or MariaDB as a database.

To run WordPress, we use the LAMP, which stands for:

- Linux – Operating System

- Apache – Web Server

- MariaDB – Database Server

- PHP – Server-side scripting language
- 
## :dart: Prerequisites

Before getting started, make sure you have:
1. An AWS account
2. Amazon linux EC2 instance
3. SSH key pair
4. A wordpress files ready for deployment.


## :bulb: Deployment Steps
### Step 1: Launch EC2 instance
- Select AMI - linux
- Key pair - firsy-cal-key.pem
- Security group - allow port httpd (80) ssh (22)
- Launch instance
  
![Reference Image](/img/img1.png)
### Step 2: Create LAMP.sh file.

```bash
sudo yum update
sudo yum install httpd mariadb105-server php -y
sudo systemctl start httpd mariadb php-fpm
sudo systemctl enable httpd mariadb php-fpm
```
```bash
sudo bash LAMP.sh
```
![Reference Image](/img/img2.png)

 ### Step 3: Install wordpress in home directory.

![Reference Image](/img/img3.png)

### Step 4: Extract the wordpress file(latest.tar.gz) & move in the html directory.

![Reference Image](/img/img4.png)

### Step 5: Copy IP address 

![Reference Image](/img/img5.png)

### Step 6: Paste the broswer and access the wordpress dashboard.

![Reference Image](/img/img6.png)

### Step 7: Create the database 

![Reference Image](/img/img7.png)

### Step 8: Data can store the database.
![Reference Image](/img/img8.png)

### Step 9: Publish the website in broswer.
![Reference Image](/img/img9.png)

## :pushpin:**Summary**
In this project, WordPress is deployed on an AWS EC2 instance using the LAMP stack. Apache handles client requests, PHP processes WordPress files, and MariaDB stores website data such as users, posts, and settings.

This setup allows us to host a dynamic website where content can be created, updated, and managed through the WordPress dashboard.