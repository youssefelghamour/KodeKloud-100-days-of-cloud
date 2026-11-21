# 100 Days of Cloud: AWS Track (Days 1-50)

![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon EC2](https://img.shields.io/badge/Amazon_EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white)
![Amazon VPC](https://img.shields.io/badge/Amazon_VPC-8C4FFF?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon RDS](https://img.shields.io/badge/Amazon_RDS-527FFF?style=for-the-badge&logo=amazon-rds&logoColor=white)
![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-FF9900?style=for-the-badge&logo=awslambda&logoColor=white)
![Amazon DynamoDB](https://img.shields.io/badge/Amazon_DynamoDB-4053D6?style=for-the-badge&logo=amazondynamodb&logoColor=white)
![Amazon ECS](https://img.shields.io/badge/Amazon_ECS-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Amazon EKS](https://img.shields.io/badge/Amazon_EKS-FF9900?style=for-the-badge&logo=amazon-eks&logoColor=white)
![AWS CloudFormation](https://img.shields.io/badge/CloudFormation-FF4F8B?style=for-the-badge&logo=amazon-aws&logoColor=white)

This repository documents my hands-on solutions for the **KodeKloud 100 Days of Cloud Challenge (50 Days of AWS Track)**. It serves as a technical log of my work managing and migrating infrastructure for **xFusionCorp Industries** within the **Stratos Datacenter**.

Each challenge is designed around real-world tickets, including provisioning core cloud infrastructure, troubleshooting network and route table issues, securing workloads, and automating deployment pipelines using a CLI-first approach backed by AWS Management Console validation.

## Core Competencies
* **Compute & Auto Scaling:** EC2 instance lifecycle management, custom AMIs, user data automation, and Auto Scaling Groups.
* **VPC Networking:** Custom VPCs, public and private subnets, Internet Gateways, NAT solutions, Route Tables, and VPC Peering.
* **Storage Systems:** S3 bucket versioning, public static hosting, cross-bucket data migration, EBS volumes, and snapshots.
* **Database Management:** Relational database setup with Amazon RDS (MySQL), DB subnet groups, storage autoscaling, and NoSQL with Amazon DynamoDB.
* **Security & Access Control:** IAM users, groups, roles, customer-managed policies, instance profiles, security group chaining, and AWS KMS encryption.
* **Serverless & Event-Driven Systems:** AWS Lambda, S3 event notifications, SQS priority queuing, SNS topic filter policies, and CloudWatch alarms.
* **Containers & Orchestration:** Amazon ECR registries, serverless container deployments with Amazon ECS (Fargate), and managed Kubernetes with Amazon EKS.
* **Infrastructure as Code:** Declarative stack deployments using AWS CloudFormation.

## Repository Structure

Every day has its own folder, named `Day N - Task Title`. The topic sections below group the days by service area and link to each folder.

Each daily folder includes a dedicated `README.md` containing:
1. **The Objective:** The specific operational ticket requirement.
2. **Diagram:** Diagram I drew for the task describing the architecture.
3. **Architectural Concepts:** Explanation of the service mechanics, configuration parameters, and principles.
4. **Command Execution:** The step-by-step AWS CLI commands used to configure the infrastructure.
5. **Dual Verification:** Command-line query outputs combined with AWS Management Console inspection steps.
6. **Screenshots:** Terminal output captures and AWS Console UI verification views.

## Topics and Days

### [Compute](./compute) (Days 1, 6, 7, 8, 9, 13, 14, 21, 22, 25, 26, 44)

This section covers virtual server provisioning and compute management. I created key pairs, launched EC2 instances across various Linux distributions, configured user data bootstrap scripts to install web servers on launch, adjusted instance types for vertical scaling, enabled stop and termination protections, built custom AMIs, built Auto Scaling Groups behind a load balancer, and performed live storage expansions using `growpart` and `xfs_growfs`.

* [Day 1 - Create Key Pair](<./Day 1 - Create Key Pair>)
* [Day 6 - Launch EC2 Instance](<./Day 6 - Launch EC2 Instance>)
* [Day 7 - Change EC2 Instance Type](<./Day 7 - Change EC2 Instance Type>)
* [Day 8 - Enable Stop Protection for EC2 Instance](<./Day 8 - Enable Stop Protection for EC2 Instance>)
* [Day 9 - Enable Termination Protection for EC2 Instance](<./Day 9 - Enable Termination Protection for EC2 Instance>)
* [Day 13 - Create AMI from EC2 Instance](<./Day 13 - Create AMI from EC2 Instance>)
* [Day 14 - Terminate EC2 Instance](<./Day 14 - Terminate EC2 Instance>)
* [Day 21 - Setting Up an EC2 Instance with an Elastic IP for Application Hosting](<./Day 21 - Setting Up an EC2 Instance with an Elastic IP for Application Hosting>)
* [Day 22 - Configuring Secure SSH Access to an EC2 Instance](<./Day 22 - Configuring Secure SSH Access to an EC2 Instance>)
* [Day 25 - Setting Up an EC2 Instance and CloudWatch Alarm](<./Day 25 - Setting Up an EC2 Instance and CloudWatch Alarm>)
* [Day 26 - Configuring an EC2 Instance as a Web Server with Nginx](<./Day 26 - Configuring an EC2 Instance as a Web Server with Nginx>)
* [Day 44 - Implementing Auto Scaling for High Availability in AWS](<./Day 44 - Implementing Auto Scaling for High Availability in AWS>)

### [Networking](./networking) (Days 2, 3, 10, 11, 24, 27, 29, 30, 36, 40, 45, 49)
This domain covers virtual network engineering in AWS. I built custom public and private VPCs, created subnets across multiple Availability Zones, configured Internet Gateways, managed route table rules, and chained security groups to protect backend targets. I also set up Elastic IPs, attached secondary ENIs, deployed Application Load Balancers with target groups, established two-way VPC Peering connections, deployed both EC2-based NAT Instances and managed AWS NAT Gateways, and troubleshot a VPC with a detached Internet Gateway.

* [Day 2 - Create Security Group](<./Day 2 - Create Security Group>)
* [Day 3 - Create Subnet](<./Day 3 - Create Subnet>)
* [Day 10 - Attach Elastic IP to EC2 Instance](<./Day 10 - Attach Elastic IP to EC2 Instance>)
* [Day 11 - Attach Elastic Network Interface to EC2 Instance](<./Day 11 - Attach Elastic Network Interface to EC2 Instance>)
* [Day 24 - Setting Up an Application Load Balancer for an EC2 Instance](<./Day 24 - Setting Up an Application Load Balancer for an EC2 Instance>)
* [Day 27 - Configuring a Public VPC with an EC2 Instance for Internet Access](<./Day 27 - Configuring a Public VPC with an EC2 Instance for Internet Access>)
* [Day 29 - Establishing Secure Communication Between Public and Private VPCs via VPC Peering](<./Day 29 - Establishing Secure Communication Between Public and Private VPCs via VPC Peering>)
* [Day 30 - Enable Internet Access for Private EC2 using NAT Instance](<./Day 30 - Enable Internet Access for Private EC2 using NAT Instance>)
* [Day 36 - Load Balancing EC2 Instances with Application Load Balancer](<./Day 36 - Load Balancing EC2 Instances with Application Load Balancer>)
* [Day 40 - Troubleshooting Internet Accessibility for an EC2-Hosted Application](<./Day 40 - Troubleshooting Internet Accessibility for an EC2-Hosted Application>)
* [Day 45 - Configure NAT Gateway for Internet Access in a Private VPC](<./Day 45 - Configure NAT Gateway for Internet Access in a Private VPC>)
* [Day 49 - Centralized Audit Logging with VPC Peering](<./Day 49 - Centralized Audit Logging with VPC Peering>)

### [Storage](./storage) (Days 4, 5, 12, 15, 23, 39, 50)

This section covers block and object storage. I configured S3 bucket versioning to safeguard files, applied public access configurations and bucket policies for static website hosting, and used `aws s3 sync` for data migrations. For block storage, I created and attached GP3 EBS volumes, configured device mappings (`/dev/sdb`), and took point-in-time EBS snapshots.

* [Day 4 - Enable Versioning for S3 Bucket](<./Day 4 - Enable Versioning for S3 Bucket>)
* [Day 5 - Create GP3 Volume](<./Day 5 - Create GP3 Volume>)
* [Day 12 - Attach Volume to EC2 Instance](<./Day 12 - Attach Volume to EC2 Instance>)
* [Day 15 - Create Volume Snapshot](<./Day 15 - Create Volume Snapshot>)
* [Day 23 - Data Migration Between S3 Buckets Using AWS CLI](<./Day 23 - Data Migration Between S3 Buckets Using AWS CLI>)
* [Day 39 - Hosting a Static Website on AWS S3](<./Day 39 - Hosting a Static Website on AWS S3>)
* [Day 50 - Expanding EC2 Instance Storage for Development Needs](<./Day 50 - Expanding EC2 Instance Storage for Development Needs>)



### [Databases](./databases) (Days 31, 32, 35, 42)

This section covers managed relational and NoSQL databases. I deployed private Amazon RDS MySQL instances using custom DB subnet groups spanning multiple Availability Zones, enabled storage autoscaling, executed manual database snapshots, restored snapshots into new database instances, connected an EC2 web application to a private RDS database, and created Amazon DynamoDB tables with custom partition keys and on-demand billing.

* [Day 31 - Configuring a Private RDS Instance for Application Development](<./Day 31 - Configuring a Private RDS Instance for Application Development>)
* [Day 32 - Snapshot and Restoration of an RDS Instance](<./Day 32 - Snapshot and Restoration of an RDS Instance>)
* [Day 35 - Deploying and Managing Applications on AWS](<./Day 35 - Deploying and Managing Applications on AWS>)
* [Day 42 - Building and Managing NoSQL Databases with AWS DynamoDB](<./Day 42 - Building and Managing NoSQL Databases with AWS DynamoDB>)


### [Security & Identity](./security-identity) (Days 16, 17, 18, 19, 20, 37, 41)
This domain covers identity and access governance. I created IAM users and groups, wrote custom IAM policies following the principle of least privilege, attached policies to identities, built IAM roles with service trust policies (`ec2.amazonaws.com`), and created instance profiles to grant EC2 instances keyless access to services. I also managed customer-managed encryption keys using AWS KMS to encrypt and decrypt sensitive files.

* [Day 16 - Create IAM User](<./Day 16 - Create IAM User>)
* [Day 17 - Create IAM Group](<./Day 17 - Create IAM Group>)
* [Day 18 - Create Read-Only IAM Policy for EC2 Console Access](<./Day 18 - Create Read-Only IAM Policy for EC2 Console Access>)
* [Day 19 - Attach IAM Policy to IAM User](<./Day 19 - Attach IAM Policy to IAM User>)
* [Day 20 - Create IAM Role for EC2 with Policy Attachment](<./Day 20 - Create IAM Role for EC2 with Policy Attachment>)
* [Day 37 - Managing EC2 Access with S3 Role-based Permissions](<./Day 37 - Managing EC2 Access with S3 Role-based Permissions>)
* [Day 41 - Securing Data with AWS KMS](<./Day 41 - Securing Data with AWS KMS>)

### [Serverless & Messaging](./serverless-messaging) (Days 33, 34, 46, 47)

This section covers event-driven architecture and asynchronous communication. I authored and deployed Python Lambda functions using both the console and the AWS CLI, configured S3 event notifications to trigger automated file copying, implemented priority message routing using Amazon SNS filter policies and Amazon SQS queues, and set up CloudWatch metric alarms to monitor CPU utilization and notify SNS topics.

* [Day 33 - Create a Lambda Function](<./Day 33 - Create a Lambda Function>)
* [Day 34 - Create a Lambda Function Using CLI](<./Day 34 - Create a Lambda Function Using CLI>)
* [Day 46 - Event-Driven Processing with Amazon S3 and Lambda](<./Day 46 - Event-Driven Processing with Amazon S3 and Lambda>)
* [Day 47 - Integrating AWS SQS and SNS for Reliable Messaging](<./Day 47 - Integrating AWS SQS and SNS for Reliable Messaging>)

### [Containers](./containers) (Days 28, 38, 43)

This folder covers containerized workflows on AWS. I created private Amazon ECR repositories, authenticated Docker, and pushed custom application images. I also set up Amazon ECS clusters, wrote task definitions, deployed services using serverless AWS Fargate, and provisioned managed Amazon EKS Kubernetes clusters with private endpoints across three Availability Zones.

* [Day 28 - Creating a Private ECR Repository](<./Day 28 - Creating a Private ECR Repository>)
* [Day 38 - Deploying Containerized Applications with Amazon ECS](<./Day 38 - Deploying Containerized Applications with Amazon ECS>)
* [Day 43 - Scaling and Managing Kubernetes Clusters with Amazon EKS](<./Day 43 - Scaling and Managing Kubernetes Clusters with Amazon EKS>)

### [Infrastructure as Code](./infrastructure-as-code) (Days 47, 48)
This section covers automated infrastructure provisioning using AWS CloudFormation. I wrote declarative YAML templates to deploy serverless applications, managed named IAM capabilities (`CAPABILITY_NAMED_IAM`), and automated multi-resource messaging and compute architectures.

* [Day 47 - Integrating AWS SQS and SNS for Reliable Messaging](<./Day 47 - Integrating AWS SQS and SNS for Reliable Messaging>) (also listed under Serverless & Messaging)
* [Day 48 - Automating Infrastructure Deployment with AWS CloudFormation](<./Day 48 - Automating Infrastructure Deployment with AWS CloudFormation>)

## Certification

![100 Days of Cloud - AWS Track Certificate](KodeKloud%2050%20Days%20of%20AWS%20Cloud.jpg)

[Verify Certificate](https://engineer.kodekloud.com/certificate-verification/46473566-de2f-4b3d-8b90-db88f18851ea)