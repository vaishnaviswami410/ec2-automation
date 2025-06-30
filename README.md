#  EC2 Automation with CloudFormation
This project automates the deployment of an EC2 instance using AWS CloudFormation. 
It includes configuration management, environment selection (Dev/Prod), Java installation, GitHub app deployment, and auto-stop for cost optimization.

**Features**

Launches EC2 instance with specified configuration

Installs Java 21 using user data script

Clones and runs an app from a GitHub repo

Automatically opens port 80 for HTTP access

Supports stage-wise config: Dev and Prod

Automatically stops instance after a set time

Keeps AWS credentials safe using environment variables

**Prerequisites**

AWS Free Tier Account

A key pair in the AWS region you’re deploying to (e.g., Mumbai)

Git installed on your machine

Basic knowledge of CloudFormation or VS Code

 **How to Run This Project**
 
1. Clone This Repository
git clone https://github.com/vaishnaviswami/ec2-automation.git
cd ec2-automation
