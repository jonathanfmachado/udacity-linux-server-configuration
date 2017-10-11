# Project: Linux Server Configuration
You will take a baseline installation of a Linux server and prepare it to host your web applications. You will secure your server from a number of attack vectors, install and configure a database server, and deploy one of your existing web applications onto it.

## IP address and SSH port ##
- Public IP: 18.220.43.67
- SSH port: 2200

## Complete URL to web application ## 
http://ec2-18-220-43-67.us-east-2.compute.amazonaws.com/catalog/

## Summary of software installed and configuration changes made ## 

- Get all system packages updates available: sudo apt-get update
- Install all system packages updates: sudo apt-get upgrade
- SSH port changed from 22 to 2200
- sudo nano /etc/ssh/sshd_config (param: Port)

- UFW configured to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
  - sudo ufw default deny incoming
  - sudo ufw default allow outgoing
  - sudo ufw allow 2200/tcp
  - sudo ufw allow www
  - sudo ufw allow 123/tcp

##  List of third-party resources used to complete this project ## 
- Git
- https://www.tecmint.com/disable-or-enable-ssh-root-login-and-limit-ssh-access-in-linux/
- http://blog.codeasite.com/how-do-i-find-apache-http-server-log-files
