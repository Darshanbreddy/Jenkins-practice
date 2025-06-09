Jenkins CI/CD Pipeline for Django Notes App
Overview
This project demonstrates a hands-on Jenkins CI/CD pipeline setup to automate building, testing, and deploying a Django Notes App using Docker and Docker Compose. The pipeline is configured using a Jenkinsfile with Groovy syntax and incorporates a shared library for better modularity.

What I Learned
Creating Jenkins Freestyle and Pipeline jobs

Setting up Jenkins Master and Slave (Agent) nodes on separate EC2 instances

Establishing connection between Master and Slave using labels

Integrating Jenkins with GitHub using webhooks for automated build triggers

Cloning GitHub repositories in Jenkins pipeline

Building Docker images and running containers as part of the Jenkins pipeline

Deploying apps using both Docker run and Docker Compose

Creating and using Jenkins Shared Libraries for reusable pipeline code

Project Details
Jenkins Setup
Master Node: Main Jenkins server running the pipeline

Agent Node: EC2 instance labeled vinod, connected as a Jenkins agent

Job Types: Freestyle job (basic directory creation) and Pipeline job (full CI/CD pipeline)

Pipeline Stages
Checkout Code
Clones the forked Django Notes App repository from GitHub.

Build
Builds a Docker image of the Django app successfully.

Test
(Optional) Run tests or validations inside the pipeline (can be added).

Deploy
Runs the Docker container on port 8000 and verifies the app is up.
Also runs the app using Docker Compose.

How to Use
Fork the Django Notes App repo from [TWS Repo] to your GitHub.

Set up Jenkins Master and Agent with appropriate labels.

Configure Jenkins pipeline job with the provided Jenkinsfile.

Add GitHub webhook for automatic builds on code push.

Push your code and watch the pipeline trigger builds, tests, and deployments automatically.

References
Train With Shubham - Jenkins CI/CD Pipeline Tutorial - The primary video tutorial followed to build this pipeline.
