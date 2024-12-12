# How I Built a Scalable Web Infrastructure for SmartShop
## Company overview
SmartShop is a fictional mid-sized retail company that has recently decided to expand its business by launching an online store. As they anticipate an increase in web traffic due to marketing campaigns and seasonal sales, SmartShop requires a robust and reliable web infrastructure to ensure smooth customer experiences. With minimal in-house IT staff and a limited budget, they seek a cost-effective solution that can be manually adjusted for growth as needed, providing high availability and essential security while keeping operational complexity low. 

## Project Objectives
The aim of the project was to design and deploy a reliable web application infrastructure on AWS, which  solution should:
Support anticipated growth with flexible resource allocation.
Ensure high availability and consistent user experience.
Implement strong security measures to protect customer data.
Be cost-effective and optimized for performance.

## Project’s Mission
The mission of the project was to develop a solution that meets SmartShop's requirements by leveraging AWS services such as EC2, Virtual Private Cloud (VPC), and Identity and Access Management (IAM). 

## Procedure
### Step 1
I set up a Virtual Private Cloud (VPC)
A virtual private cloud was created to host SmartShop’s Infrastructure. The VPC was divided into public and private subnets across multiple availability zones for redundancy. 
Then, Internet Gateways were set up to allow internet access to public subnets,and Route Tables were configured to manage traffic flow between subnets and the internet.

### Step 2
I navigated to the security group panel and clicked on Security group. 
<img src="images/LITA 1.JPG">

I choose the option to create a new security group and I edited it as follows;
<img src="images/LITA 2.JPG">

I edited the inbound rules to allow SSH and HTTP traffic from anywhere in the world.
<img src="images/LITA 3.JPG">

And the outbound rule was set to allow all traffic.
<img src="images/LITA 4.JPG">

Then I clicked on create security group and my security group was successfully created. 
<img src="images/LITA 5.JPG">

### Step 3
I launched an EC2 Instance
On the EC2 dashboard, I clicked on instances, and the button to launch an instance. 
<img src="images/LITA 6.JPG">

I filled in the name of my EC2 intsnce, selected Amazon Linux 2 as the AMI, and I created a new key pair.
<img src="images/LITA 7.JPG">
<img src="images/LITA 8.JPG">
<img src="images/LITA 9.JPG">

I selected the key pair i just created and edited my network settings as follows
<img src="images/LITA 10.JPG">
 
 I configured my network settings as follows; and selected the security group I created earlier.
<img src="images/LITA 11.JPG">

I made no changes to Storage and advanced details and clicked on launch instance. 
<img src="images/LITA 12.JPG">

Now my instance has beem successfully created aand initialized.
<img src="images/LITA 13.JPG">
<img src="images/LITA 14.JPG">

I clicked on connect and selected SSH client.
Then,I accessed the key pair file i downloaded earlier and opened VS Code through it. 
<img src="images/LITA 15.JPG">

I ran the command to ensure that my key is not publicly viewable.
<img src="images/LITA 16.JPG">

I ran the other command to connect to my instance using ssh and the connection was successful. 
<img src="images/LITA 17.JPG">

Then I ran the following commands to install apache
<img src="images/LITA 18.JPG">

And my apache installation was successful
<img src="images/LITA 19.JPG">

I went back to the instance dashboard and copied the public IP address of my EC2 instance. 
<img src="images/LITA 20.JPG">

I pasted the link in my browser and the test page was displayed.
<img src="images/LITA 21.JPG">

I terminated my EC2 intance, and deleted the security group.  
<img src="images/LITA 22.JPG">

This marked the end of the project.

## Thank You!


