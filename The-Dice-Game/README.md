# Dice Game Cloud Deployment on AWS

# Overview

This project demonstrates the deployment of a static web application (Dice Game) on AWS using a modern, production-ready cloud architecture. The solution ensures high availability, global accessibility, secure HTTPS communication, and automated deployments using CI/CD.

# Live Demo

# CloudFront URL: https://d19i8blrxsc1k2.cloudfront.net

# Architecture

The application follows a standard static hosting architecture:

User → Route 53 → CloudFront → S3

Amazon S3 stores the static website files
Amazon CloudFront delivers content globally with low latency
Amazon Route 53 handles domain name resolution
AWS Certificate Manager (ACM) provides SSL/TLS encryption
AWS IAM manages secure access control
GitHub Actions* automates deployment


# Deployment Process

 1. Clone the Repository

```bash
git clone https://github.com/feyiwaves/dice-game-cloud-deployment.git
cd dice-game-cloud-deployment
```

 2. S3 Bucket Configuration

Created an S3 bucket for static hosting
Uploaded HTML, CSS, and JavaScript files
Disabled public access to the bucket
Configured access through CloudFront only

 3. CloudFront Setup

Created a CloudFront distribution
Configured S3 as the origin
Enabled caching for improved performance
Enforced HTTPS access

 4. Route 53 (Optional)

Configured hosted zone
Mapped domain to CloudFront distribution

 5. CI/CD Pipeline (GitHub Actions)

The deployment process is fully automated using GitHub Actions.

# Trigger:

# Push to `main` branch

# Workflow:

Checkout source code
Configure AWS credentials securely
Upload updated files to S3
Invalidate CloudFront cache


# Security Implementation

S3 bucket is private
Access restricted using CloudFront Origin Access 
HTTPS enforced 
IAM roles follow least privilege principle
Credentials stored securely using GitHub Secrets


# Author
Feyiwaves 
