# LAMP Stack Implementation in AWS
This project outlines steps to setup LAMP stack on an AWS EC2 instance running ubuntu.

LAMP stands for Linux, Apache, MySQL and PHP

The setup is going to be done on an AWS EC2 instance running Ubuntu

## Connect to the EC2 instance through SSH
```
ssh -i "<private_key_file_name> ubuntu@<public_ip_address>
```
## Install Apache and update firewall
Steps to installing apache

1. update the local package index
```
sudo apt update
```
2. Install apache
```
sudo apt install apache2
```
3. Check if apache2 is running
```
systemctl status apache2
```
![apache Status screenshot](images/check_apache_status.png)

For Apache to serve web pages through the browser, the EC2 instance must be able to accept incoming requests through port 80 which is the default port for HTTP traffic. This can be done by updating the inbound rules of the EC2 instance. Inbound rules can be found under security group
![Alt](images/inbound_rules.png)


To view  the apache homepage, enter go to the public IP adrress in the browser over http
http://<public_ip_addres>

