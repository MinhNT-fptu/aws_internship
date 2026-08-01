---
title: "Week 12 Worklog"
date: "2026-08-06"
weight: 12
chapter: false
pre: " <b> 1.12. </b> "
---

### Objectives for Week 12:

* Research and design an AWS architecture for the project's development and testing environment.
* Identify the connection flows between the frontend, backend, storage system, and MongoDB Atlas.
* Deploy the project's frontend and backend to AWS based on the designed architecture.
* Configure networking, security, secret management, and access permissions.
* Set up system monitoring, alerts, and AWS cost tracking.
* Verify the system's functionality after deployment to AWS.

### Tasks to be completed this week:

| Day       | Tasks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Start date | Completion date | Reference materials |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------- |
| Monday    | - Analyze the project deployment requirements for the AWS development and testing environment. <br> - Identify the main system components, including the S3 Frontend Bucket, S3 Receipts Bucket, VPC, Public Subnet, Internet Gateway, EC2, Elastic IP, and MongoDB Atlas. <br> - Analyze the access flows from users to the frontend and backend. <br> - Select the AWS Region `ap-southeast-1` for resource deployment.                                                                                                                                                                                                                | 01/08/2026 | 01/08/2026      |                     |
| Tuesday   | - Research and create the overall architecture diagram for the development and testing environment. <br>&emsp; + Design the frontend to be hosted in the S3 Frontend Bucket. <br>&emsp; + Design the backend to be deployed on EC2 within a Public Subnet. <br>&emsp; + Connect the Public Subnet to an Internet Gateway. <br>&emsp; + Assign an Elastic IP to EC2 to provide a fixed public IP address. <br>&emsp; + Design the S3 Receipts Bucket for storing receipt images. <br>&emsp; + Illustrate the connection between the EC2 backend and MongoDB Atlas. <br> - Review and finalize the architecture diagram before deployment. | 02/08/2026 | 02/08/2026      |                     |
| Wednesday | - Deploy the network infrastructure and backend on AWS. <br>&emsp; + Create a VPC and Public Subnet. <br>&emsp; + Create and attach an Internet Gateway to the VPC. <br>&emsp; + Configure the route table so that the Public Subnet can access the Internet. <br>&emsp; + Create a Web Security Group and restrict the allowed access ports. <br>&emsp; + Launch an EC2 instance and assign an Elastic IP. <br>&emsp; + Configure the backend runtime environment on EC2. <br>&emsp; + Deploy the backend source code and test the APIs.                                                                                                | 03/08/2026 | 03/08/2026      |                     |
| Thursday  | - Deploy the frontend and storage system on AWS. <br>&emsp; + Create an S3 Frontend Bucket to store the frontend build files. <br>&emsp; + Build and upload the frontend application to S3. <br>&emsp; + Create an S3 Receipts Bucket to store receipt images uploaded by users. <br>&emsp; + Create an IAM Role and grant the required permissions for EC2 to access the S3 Receipts Bucket. <br>&emsp; + Use Secrets Manager to manage sensitive backend information. <br>&emsp; + Configure the connection from EC2 to MongoDB Atlas. <br> - Test the frontend-to-backend API flow and the receipt image upload flow.                 | 04/08/2026 | 04/08/2026      |                     |
| Friday    | - Configure system management, monitoring, and alerting. <br>&emsp; + Use CloudWatch to monitor EC2 metrics and backend logs. <br>&emsp; + Configure CloudWatch alarms for the required metrics. <br>&emsp; + Connect CloudWatch to SNS to send notifications when alarms are triggered. <br>&emsp; + Configure AWS Budgets to monitor AWS usage costs and send cost alerts. <br> - Test the complete system after deployment. <br> - Record issues, apply fixes, and complete the deployment documentation.                                                                                                                             | 05/08/2026 | 05/08/2026      |                     |

### Results achieved in Week 12:

* General results:
  * This week, I focused on researching, designing, and deploying an AWS architecture for the project's development and testing environment.
  * I completed an architecture diagram that includes frontend, backend, storage, database, networking, security, monitoring, and cost-management components.
  * The project's frontend and backend were deployed to AWS according to the designed architecture.
  * The system was able to connect to MongoDB Atlas, store receipt images in S3, and be monitored through CloudWatch.

* Designed architecture:
  * Used AWS Region `ap-southeast-1` to deploy the resources.
  * Used the S3 Frontend Bucket to store the frontend application's static files.
  * Used the S3 Receipts Bucket to store receipt images and files uploaded by users.
  * Deployed the backend on an EC2 instance within a Public Subnet in the VPC.
  * Used an Internet Gateway to allow resources in the Public Subnet to access the Internet.
  * Used an Elastic IP to provide a fixed public IP address for the EC2 instance.
  * Used a Web Security Group to control inbound and outbound traffic for EC2.
  * Connected the backend hosted on EC2 to MongoDB Atlas.
  * Used an IAM Role to grant EC2 access to the required AWS services.
  * Used Secrets Manager to manage sensitive application information.
  * Used CloudWatch, SNS, and AWS Budgets to monitor system activity and AWS costs.

* Completed deployment tasks:
  * Created the VPC, Public Subnet, Internet Gateway, and route table.
  * Created and configured the Security Group for the backend.
  * Launched an EC2 instance and assigned an Elastic IP.
  * Configured the runtime environment and deployed the backend to EC2.
  * Created the S3 Frontend Bucket and deployed the frontend to S3.
  * Created the S3 Receipts Bucket for receipt image storage.
  * Created an IAM Role and granted EC2 permission to access S3.
  * Configured the backend settings and sensitive information.
  * Connected the backend to MongoDB Atlas.
  * Tested the frontend-to-backend request flow.
  * Tested the receipt image upload and retrieval functions using S3.
  * Configured CloudWatch to collect metrics and logs.
  * Connected CloudWatch alarms to SNS.
  * Configured AWS Budgets to monitor usage costs.

* System operation flow:
  * Users access the frontend hosted in the S3 Frontend Bucket.
  * The frontend sends API requests to the backend through the EC2 instance's Elastic IP.
  * The Internet Gateway supports Internet connectivity for the EC2 instance in the Public Subnet.
  * The backend processes business logic and connects to MongoDB Atlas to retrieve or store data.
  * The backend uses an IAM Role to upload and retrieve receipt images from the S3 Receipts Bucket.
  * Sensitive application information is managed through Secrets Manager.
  * CloudWatch collects metrics and logs from EC2.
  * SNS sends notifications when system alarms are triggered.
  * AWS Budgets monitors costs and sends alerts when spending reaches the configured threshold.

* Knowledge and experience gained:
  * Gained a better understanding of how to design an AWS architecture for a development and testing environment.
  * Gained experience in deploying a static frontend application on Amazon S3.
  * Gained experience in deploying a backend application on EC2 and configuring networking within a VPC.
  * Understood how to use an Internet Gateway, route table, Elastic IP, and Security Group.
  * Learned how to use an IAM Role to grant EC2 permissions without storing Access Keys in the source code.
  * Understood how to manage sensitive information using Secrets Manager.
  * Gained experience in connecting an application hosted on AWS to MongoDB Atlas.
  * Learned how to use CloudWatch and SNS for monitoring and alert notifications.
  * Understood how to use AWS Budgets to monitor and control costs.
  * Gained more experience in testing and troubleshooting a project after deploying it to AWS.