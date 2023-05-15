---
title: Deploying a Kali Linux VPS on AWS using CloudFormation
publishDate: 15 May 2023
description: We will walk you through deploying Kali Linux to an AWS VPS with a CloudFormation template.
tags: ['shorts', 'AWS', 'kali', 'linux', 'AWS-CLI', 'cloudformation', 'template', 'vps', 'deployment']
---

Kali Linux, a popular and powerful penetration testing and security auditing platform, is essential for modern cybersecurity professionals. With its vast array of tools and utilities, Kali Linux has become the go-to choice for many ethical hackers, security researchers, and network administrators. This article will walk you through deploying a Kali Linux Virtual Private Server (VPS) on Amazon Web Services (AWS) using an AWS CloudFormation template, making it easy and efficient to set up and manage your Kali Linux environment.

Prerequisites:

Before starting the deployment process, ensure you have the following:

1.  An AWS account: If you don't have one, sign up for a free tier account at [https://aws.amazon.com/](https://aws.amazon.com/).
2.  AWS CLI installed and configured: Follow the instructions at [https://aws.amazon.com/cli/](https://aws.amazon.com/cli/) to install and configure the AWS Command Line Interface (CLI) on your machine.
3.  Some knowledge of AWS CloudFormation: Familiarize yourself with AWS CloudFormation concepts and terminology at [https://aws.amazon.com/cloudformation/](https://aws.amazon.com/cloudformation/).

Step 1: Prepare the AWS CloudFormation Template

AWS CloudFormation allows you to create and manage infrastructure resources using code in the form of templates. For this deployment, we'll use a pre-built CloudFormation template specifically designed for deploying a Kali Linux VPS on AWS. The template will create an EC2 instance with the Kali Linux image and all necessary configurations.

1.  Download the CloudFormation template for Kali Linux VPS from [https://github.com/awslabs/aws-cloudformation-templates/blob/master/aws/services/EC2/Kali-Linux-VPS.yaml](https://github.com/awslabs/aws-cloudformation-templates/blob/master/aws/services/EC2/Kali-Linux-VPS.yaml)
2.  Save the downloaded template on your local machine.

Step 2: Launch the Kali Linux VPS Stack

Now that you have the CloudFormation template, you can launch the Kali Linux VPS stack using the AWS Management Console or the AWS CLI.

Using the AWS Management Console:

1.  Log in to your AWS Management Console and navigate to the CloudFormation service.
2.  Click on "Create stack" and select "With new resources (standard)".
3.  In the "Specify template" section, choose "Upload a template file" and upload the downloaded CloudFormation template.
4.  Click "Next" to proceed.
5.  Enter a stack name, such as "KaliLinuxVPS".
6.  Configure any additional parameters as needed. For example, you can specify the instance type, key pair, and VPC settings.
7.  Click "Next" to proceed to the "Configure stack options" page, where you can configure tags, permissions, and other advanced options.
8.  Click "Next" to review your stack settings. Confirm that everything is correct and click "Create stack" to launch the Kali Linux VPS.

Using the AWS CLI:

1.  Open a terminal or command prompt on your machine.
2.  Run the following command to create the Kali Linux VPS stack, replacing "your-key-pair" with the name of the AWS key pair you want to use, and "path/to/Kali-Linux-VPS.yaml" with the path to the downloaded CloudFormation template:

```shell
aws cloudformation create-stack --stack-name KaliLinuxVPS --template-body file://path/to/Kali-Linux-VPS.yaml --parameters ParameterKey=KeyName,ParameterValue=your-key-pair --capabilities CAPABILITY_IAM
```

3.  The command will return a StackId, which you can use to track the progress of the stack creation.

Step 3: Monitor the Stack Creation

Once you have initiated the stack creation process, it might take a few minutes for the resources to be provisioned. You can monitor the progress of your stack creation using the AWS Management Console or the AWS CLI.

Using the AWS Management Console:

1.  Navigate to the CloudFormation service in your AWS Management Console.
2.  Click on the stack name you provided in step 2.
3.  In the "Events" tab, you can see the real-time status of the stack creation process.

Using the AWS CLI:

1.  Run the following command, replacing "KaliLinuxVPS" with the stack name you provided in step 2:

```shell
aws cloudformation describe-stack-events --stack-name KaliLinuxVPS
```

2.  The command will return a list of events related to the stack creation process, showing the progress in real-time.

Step 4: Access the Kali Linux VPS

Once the stack creation process is complete, you can access your Kali Linux VPS using the Elastic IP address assigned to the instance.

1.  Navigate to the EC2 service in your AWS Management Console.
2.  Click on "Instances" in the left navigation pane.
3.  Locate your Kali Linux VPS instance and note the Elastic IP address in the "IPv4 Public IP" column.
4.  Open a terminal or command prompt on your machine.
5.  Use an SSH client to connect to the Kali Linux VPS using the Elastic IP address and your private key file. Replace "path/to/your-private-key" with the path to your private key file and "your-elastic-ip" with the Elastic IP address you noted earlier:

```shell
ssh -i <path/to/your-private-key> kali@<your-elastic-ip>
```

6.  Once connected, you can begin using your Kali Linux VPS for penetration testing, security auditing, or other tasks.

Conclusion:

This article has walked you through the process of deploying a Kali Linux Virtual Private Server (VPS) on AWS using an AWS CloudFormation template. By leveraging AWS CloudFormation, you can easily manage and scale your Kali Linux VPS, making it an excellent choice for cybersecurity professionals and enthusiasts alike.
