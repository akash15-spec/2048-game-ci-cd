🎮 2048 Game CI/CD Pipeline on AWS (Docker + ECS + CodePipeline)

A fully automated CI/CD pipeline for deploying a Dockerized 2048 game on AWS using Amazon ECS (Fargate), Amazon ECR, AWS CodeBuild, and AWS CodePipeline.

This project demonstrates how to build, containerize, and continuously deploy an application using modern DevOps practices, reducing manual effort and enabling fast, reliable releases.

📌 Project Overview

This project focuses on designing and implementing an end-to-end CI/CD pipeline that automates the deployment of a containerized web application (2048 game) to AWS.

The pipeline handles:

Building a Docker image

Pushing the image to Amazon ECR

Deploying the container to Amazon ECS using Fargate

Automating the entire workflow using AWS CodePipeline

The result is a scalable, serverless container deployment that updates automatically whenever new changes are pushed.

🏗️ Architecture Overview
High-Level Design
Developer
 │
 ▼
Source Code (GitHub)
 │
 ▼
AWS CodePipeline
 │
 ├── CodeBuild (Build & Docker Image)
 │
 ├── Amazon ECR (Container Registry)
 │
 └── Amazon ECS (Fargate)
       └── 2048 Game Container

☁️ AWS Services Used

AWS CodePipeline – Orchestrates the CI/CD workflow (source → build → deploy)

AWS CodeBuild – Builds the Docker image and pushes it to ECR

Amazon ECR – Stores and manages Docker images

Amazon ECS (Fargate) – Runs the containerized application without managing servers

IAM Roles & Policies – Secure communication between AWS services

🚀 Key Features

✅ End-to-end CI/CD automation

✅ Dockerized application deployment

✅ Serverless container execution using Fargate

✅ Automated image build and push to ECR

✅ Scalable and production-style architecture

✅ Minimal manual intervention

🛠️ Implementation Steps
1️⃣ Set Up ECS Cluster & ECR Repository

Create an ECS cluster using Fargate

Create an ECR repository to store Docker images

Configure IAM roles for ECS and CodeBuild

2️⃣ Prepare the 2048 Game Code

Dockerize the 2048 game using a Dockerfile

Test the container locally

Push code to GitHub

3️⃣ Set Up CodeBuild (Continuous Integration)

Configure a buildspec.yml

Build Docker image

Authenticate to ECR

Push the image to ECR

4️⃣ Set Up CodePipeline (Continuous Deployment)

Connect GitHub as the source

Trigger builds automatically on code changes

Deploy updated containers to ECS

📂 Repository Structure
game-ci-cd/
│
├── app/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── Dockerfile
├── buildspec.yml
├── ecs-task-definition.json
├── README.md

🎯 Final Result

Once the pipeline is successfully built:

The 2048 game runs as a Docker container on ECS

Any new code change automatically triggers:

Image rebuild

Image push to ECR

Deployment to ECS

The game is accessible via the ECS service endpoint

This provides a real-world CI/CD deployment experience using AWS-native tools.

💰 Estimated Time & Cost
        Category	Estimate
        Setup Time	2–3 hours
        AWS Cost	~$1 or less
        Compute	AWS Fargate (minimal usage)
        Build	AWS CodeBuild (short builds)

🎓 Learning Outcomes

Through this project, you gain hands-on experience with:

   CI/CD pipeline design using AWS

   Docker containerization

   ECS & Fargate deployment models

   Infrastructure automation concepts

   Secure IAM role configuration

   Real-world DevOps workflows


📈 Future Enhancements

  🔐 HTTPS with Application Load Balancer

  📊 CloudWatch logging and monitoring

  🧪 Automated testing stage in CodePipeline

  🔄 Blue/Green deployments

  ⚙️ Infrastructure as Code using Terraform or CloudFormation

-->📚 Acknowledgements & Learning Resources

 -This project was implemented as part of advanced hands-on learning inspired by Techwith Lucy – AWS Advanced Projects.

The learning material helped reinforce:

 --CI/CD pipeline architecture

 --Docker and container workflows

 --ECS and Fargate deployment strategies

AWS DevOps best practices

All implementation, configuration, and deployment steps were performed independently for hands-on learning and portfolio development.
