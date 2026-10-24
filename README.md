
# Docker Image Management Using Amazon ECR

## Project Overview
This project demonstrates how to build a simple web application,
containerize it using Docker, and upload the Docker image to
Amazon Elastic Container Registry (Amazon ECR).

## Technologies Used
- Docker
- Docker Desktop
- Amazon Web Services (AWS)
- Amazon ECR
- AWS CLI
- AWS IAM
- HTML and CSS
- Git and GitHub

## Project Architecture
Local Web Application -> Docker Image -> Amazon ECR Repository

## Project Steps
1. Created a simple HTML web application.
2. Created a Dockerfile using the Nginx Alpine image.
3. Built and tested the Docker image locally.
4. Configured AWS CLI credentials.
5. Created a private Amazon ECR repository.
6. Configured IAM permissions for ECR access.
7. Authenticated Docker to Amazon ECR.
8. Tagged and pushed the image to ECR.
9. Verified the image in the AWS Console.

## Build the Docker Image
```bash
docker build -t docker-ecr-web:v1 .
```

## Run the Application Locally
```bash
docker run -d --name ecr-web-test -p 8080:80 docker-ecr-web:v1
```

Open http://localhost:8080 in your browser.

## AWS ECR Workflow
Authenticate Docker to your ECR registry, tag the image
with your registry URI, and push it to your repository.

Use the official AWS ECR documentation:
https://docs.aws.amazon.com/AmazonECR/latest/userguide/getting-started-cli.html


