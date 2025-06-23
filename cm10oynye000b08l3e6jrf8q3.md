---
title: "Mastering Terraform Basics - Day 3"
seoTitle: "Terraform Basics: Day 3 Insights"
seoDescription: "Install Terraform on AWS EC2: launch instance, connect via SSH, update system, install Terraform"
datePublished: Fri Sep 13 2024 12:25:20 GMT+0000 (Coordinated Universal Time)
cuid: cm10oynye000b08l3e6jrf8q3
slug: mastering-terraform-basics-day-3
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1726155115774/79073f5b-065a-4df6-b6e6-8422e99fa26b.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1726155266876/3277f446-4ca1-4d29-bace-4bef085dcab3.png
tags: cloudformation, cloud, aws, cloud-computing, devops, terraform, aws-lambda, devops-articles, terraform-state, terraform-cloud, devops-trends, devops-journey, aws-devops, terraform-module, devopscommunity

---

## Installing Terraform on an AWS EC2 Instance

Terraform is a powerful Infrastructure as Code (IaC) tool that allows you to define and provision infrastructure using a declarative configuration language. In this article we will go through installing Terraform on an AWS EC2 instance, covering all dependencies and commands required.

### Prerequisites

1. **AWS Account**: Ensure you have an AWS account. You’ll need it to create and manage EC2 instances.
    
2. **EC2 Instance**: Create an EC2 instance running a Linux-based OS, such as Ubuntu, Amazon Linux, or CentOS.
    
3. **SSH Key**: You need an SSH key to securely connect to your EC2 instance.
    
4. **Basic AWS and Linux Knowledge**: Familiarity with AWS EC2, SSH, and basic Linux commands will help in following along.
    

### Step 1: Launch an AWS EC2 Instance

1. **Sign in** to the [AWS Management Console](https://aws.amazon.com/console/).
    
2. Navigate to **EC2 Dashboard** by searching for EC2 under Services.
    
3. Click **Launch Instance** to create a new EC2 instance.
    
4. Choose an **Amazon Machine Image (AMI)**. For this guide, we'll use **Ubuntu Server 22.04 LTS**:
    
    * **Ubuntu 22.04 LTS** (64-bit x86).
        
5. Choose an **Instance Type**:
    
    * For basic testing, you can use the **t2.micro** type, which falls under AWS's Free Tier.
        
6. **Configure Instance Details**:
    
    * Accept the default settings.
        
7. **Add Storage**:
    
    * Leave the default (8 GB EBS volume) unless you require additional storage.
        
8. **Add Tags**:
    
    * Optionally, you can add tags to identify this instance.
        
9. **Configure Security Group**:
    
    * Ensure that port **22 (SSH)** is open to allow SSH access. Optionally restrict SSH access to your IP.
        
10. **Review and Launch**:
    
    * Click **Launch** and download the **key pair** when prompted. This key pair (.pem file) is necessary to access your EC2 instance.
        

### Step 2: Connect to Your EC2 Instance

Once your EC2 instance is launched, you’ll connect via SSH using the key pair.

1. Open a terminal (Linux/macOS) or an SSH client like PuTTY (Windows).
    
2. Connect using the following SSH command:
    
    ```plaintext
    ssh -i /path/to/your-key.pem ubuntu@your-ec2-public-dns
    ```
    
    Replace `/path/to/your-key.pem` with the path to your SSH key file, and `your-ec2-public-dns` with the EC2 instance’s public DNS or IP address (available in the EC2 dashboard).
    
    **Note:** Ensure that your key file has the correct permissions. You may need to run:
    
    ```plaintext
    chmod 400 /path/to/your-key.pem
    ```
    

### Step 3: Update the System and Install Dependencies

Once connected to the EC2 instance, the first step is to update the package lists and install required utilities.

1. **Update the system** to ensure all packages are up-to-date:
    
    ```plaintext
    sudo apt update && sudo apt upgrade -y
    ```
    

### Step 4: Install Terraform

Now, we will install Terraform on the EC2 instance.

1. Create a .sh file using following command vim terraform.sh and paste the below script and the save the .sh file to install the terraform on ec2 instance.
    
    ```plaintext
    #Use this script to Download and install terraform
    sudo apt-get update && sudo apt-get install -y gnupg software-properties-common
    wget -O- https://apt.releases.hashicorp.com/gpg | \
    gpg --dearmor | \
    sudo tee /usr/share/keyrings/hashicorp-archive-keyring.gpg
    
    gpg --no-default-keyring \
    --keyring /usr/share/keyrings/hashicorp-archive-keyring.gpg \
    --fingerprint
    
    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] \
    https://apt.releases.hashicorp.com $(lsb_release -cs) main" | \
    sudo tee /etc/apt/sources.list.d/hashicorp.list
    
    sudo apt update
    sudo apt-get install terraform
    ```
    
2. **And run the terraform.sh file** using following command- sh terraform.sh to install the terraform.
    
3. **Verify that Terraform is installed correctly** by checking its version:
    
    ```plaintext
    terraform -v
    ```
    
    If installed correctly, you will see output similar to:
    
    ```plaintext
    Terraform v1.9.5
    ```
    

That’s it for now, thanks for following along.

---

### Conclusion

In this article we have gone through how to install Terraform on an AWS EC2 instance.

Please do follow for the upcoming posts in this Terraform Zero to Hero Series.