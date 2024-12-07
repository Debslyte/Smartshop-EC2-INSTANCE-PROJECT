# Smartshop-EC2-INSTANCE-PROJECT

This project showcases the provisioning of EC2 instance in the AWS environment

## Setting up my EC2 instance and deployed an Apache web server

The document explains how the security group was set up, also how the EC2 instance was set up and how Apache web server was deployed on it.

### Setting Up Security Groups

• I Created a new Security Group, then put in the description as “Allow SSH and HTTP traffic”

• I selected the already created VPC titled Lita_project_vpc

• Created my inbound rule, allowing SSH and HTTP traffic from anywhere IPV4

![alt text](image.png)

• I left the outbound rule with the default of allowing all traffic

![alt text](image-2.png)

• Thereafter I clicked on create Security Group

### Launching the EC2 Instance

• I named my instance using DeborahJesusolu_lita

![alt text](image-3.png)

• I choose the Amazon Linux 2 AMI under the Amazon Machine Image

![alt text](image-4.png)

• Selected the t2 micro Instance type

![alt text](image-5.png)

• Created a key pair which was downloaded

![alt text](image-6.png)

### Network Settings

• I edited my network setting (ensuring that I am not using the default setting)

• Choose the already created lita_project_vpc

• I ensured that a public subnet was selected (so as to ensure that it could be accessed through the internet.

• Auto assign public IP was enabled

### Firewall (Security Group)

• I selected existing security group

• Choose the security group I created earlier

![alt text](image-7.png)

### Configure Storage

• I left my configure storage as it was

![alt text](image-8.png)

### Final Steps

• I went back to the instance created

• Waited for it to complete initializing

• After obtaining the 2/2 score

• I clicked on that particular instance

• Went to SSH client

![alt text](image-9.png)

• Copied the code that says “Run this command, if necessary, to ensure your key is not publicly viewable.” To my Gitbash (I opened my gitbash by right clicking on an empty space in my download folder) and clicked on enter

• I thereafter copied the example link containing my key pair, ran it on Gitbash.

• My network was poor, hence brought errors, but it eventually went through, giving the bird like figure

![alt text](image-10.png)

• Typed in “sudo yum update :y” in order to ensure that it is fully updated

![alt text](image-11.png)

• Then I installed the Apache server by tying “sudo yum install httpd :y”

![alt text](image-12.png)

• I typed y, to the question “Is it ok” then it completed running

![alt text](image-13.png)

• Typed this codes to start and enable httpd “sudo systemctl start httpd
sudo systemctl enable httpd”

![alt text](image-14.png)

• To ensure that Apache has been successfully installed

• I went to my instance

• Copied the public IP address

• Then pasted it in my browser

![alt text](image-15.png)

• Finally exited my Gitbash by typing “exit”

![alt text](image-16.png)
