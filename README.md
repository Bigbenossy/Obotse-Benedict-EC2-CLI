# How To Lunch AWS EC2 Instance Command Line Interface (CLI)

## Step 0: Prerequisities 
- Install The AWS Command Line Interface (CLI) If Not Already Installed On your Computer
- The AWS CLI can be downloaded from the AWS Official Website if not already installed on your Computer

## Step 1: Configure AWS CLI Using Your IAM Credentials:
- aws –version to confirm version installed
- aws configure to configure AWS CLI

![Alt text](Images/2023-10-08.png)


![Alt text](<Images/2023-10-08 (26).png>)


## Step 2: Create Key Pair
- When creating Key Pair use the Line Command: "aws ec2 create-key-pair --key-name <keypair-Name> --query 'KeyMaterial' –output text > keypair-Name.pem ”

![Alt text](<Images/2023-10-08 (2).png>)


![Alt text](<Images/2023-10-08 (3).png>)


## Step 3: Create Security group 
- When creating security groups use the Line Command: "aws ec2 create-security-group --group-name <security Group Name> --description "Description"" 

![Alt text](<Images/2023-10-08 (4).png>)


![Alt text](<Images/2023-10-08 (5).png>)


## Step 4: Add Inbound Rule
- To Add inbound rule use the Line Command: “aws ec2 authorize-security-group-ingress --group-id <security group Id> --protocol tcp --port <port Number> --cidr <ip address>”

![Alt text](<Images/2023-10-08 (7).png>)


## Step 5: Launch Instance
- To Launch Instance use the Line Command: "aws ec2 run-instances --image-id <ami-Id> --count 1 --instance-type <type> --keyname <keypair-Name> --security-groups <security grp Name>"

![Alt text](<Images/2023-10-08 (10).png>)


![Alt text](<Images/2023-10-08 (8).png>)


![Alt text](<Images/2023-10-08 (11).png>)


![Alt text](<Images/2023-10-08 (13).png>)


## Step 6: View Running Instance
- To view the Details of the Running Instance use the Line Command:"aws ec2 describe-instances"

![Alt text](<Images/2023-10-08 (14).png>)


![Alt text](<Images/2023-10-08 (16).png>)


## Step 7: Terminate Running Instance
- To Terminate the Running Instance use the Line Command:"aws ec2 terminate-instances --instance-ids <Instance-Id> "

![Alt text](<Images/2023-10-08 (17).png>)


![Alt text](<Images/2023-10-08 (19).png>)


## Step 8: Delete Key Pair
- To Delete key pair of the Instance use the Line Command: "aws ec2 delete-key-pair --key-name <keypair-Name>"

![Alt text](<Images/2023-10-08 (20).png>)


![Alt text](<Images/2023-10-08 (22).png>)


## Step 9: Delete Security Group
- To Delete key pair of the Instance use the Line Command: "aws ec2 delete-security-group --group-name <security group Name>"

![Alt text](<Images/2023-10-08 (23).png>)


![Alt text](<Images/2023-10-08 (25).png>)

