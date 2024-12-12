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
I choose the option to create a new security group and i edited it as follows;
<img src="images/LITA 2.JPG">
I edited the inbound rules to allow SSH and HTTP traffic from anywhere in the world.
<img src="images/LITA 3.JPG">
And the outbound rule was set to allow all traffic.
<img src="images/LITA 4.JPG">
Then I clicked on create security group and my security group was successfully created. 
<img src="images/LITA 5.JPG">




