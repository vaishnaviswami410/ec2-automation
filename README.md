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

2. Update Configuration
Edit the file:

dev_config.yaml or prod_config.yaml based on your stage

Update:

InstanceType

KeyName

RepoURL (optional)

StageTimeout (e.g., 3600 seconds)

3. Deploy with CloudFormation
Log in to your AWS Console → CloudFormation → Create Stack

Select: With new resources (standard)

Choose: Upload a template file

Upload: ec2-template.yaml

Parameters:

Select Stage as either Dev or Prod

Enter a valid KeyPairName (must exist in the selected region)

4. Access Your Application
Once stack is created:

Go to EC2 Console

Find the Public IPv4 address

Open your browser and go to:

http://<public-ip>

**Notes**
No AWS keys are stored in this repo; all credentials are sourced from local environment setup.

Make sure your Security Group allows inbound traffic on ports 22 (SSH) and 80 (HTTP)

