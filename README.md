# AWS Serverless Cloud Portfolio

## Project Overview

A personal portfolio website designed and deployed using AWS cloud services. This project demonstrates practical experience with serverless architecture, cloud hosting, API integration, database operations, security and automated deployment.

## Architecture

The project uses AWS managed and serverless services to host the website and support backend functionality.

- **Amazon S3** — Stores the static website files.
- **Amazon CloudFront** — Distributes website content globally.
- **AWS Certificate Manager (ACM)** — Provides the SSL/TLS certificate for HTTPS.
- **Amazon Route 53** — Manages DNS for the custom domain.
- **Amazon API Gateway** — Exposes HTTP endpoints for backend functionality.
- **AWS Lambda** — Runs Python functions to process requests.
- **Amazon DynamoDB** — Stores visitor-counter data.
- **Amazon SES** — Sends contact-form messages by email.
- **AWS IAM** — Controls permissions for AWS resources.
- **GitHub Actions** — Automates website deployment to Amazon S3 and CloudFront cache invalidation.

## Key Features

### Static Website Hosting
Hosted the portfolio website using Amazon S3 and Amazon CloudFront, with HTTPS enabled through AWS Certificate Manager and a custom domain configured through Route 53.

### Serverless Visitor Counter
Implemented a visitor-counter API using API Gateway, a Python-based Lambda function and DynamoDB. The counter uses an atomic database update to increment the stored visitor count.

### Contact Form
Integrated a contact form with API Gateway, AWS Lambda and Amazon SES to process submissions and send email notifications.

### Automated Deployment
Configured a GitHub Actions workflow to automate website updates to Amazon S3 and invalidate the CloudFront cache after deployment.

### Security
Used AWS IAM permissions to control access between services and applied least-privilege principles where appropriate.

## Technologies Used

- **Cloud:** Amazon Web Services (AWS)
- **Compute:** AWS Lambda, Python
- **Storage and database:** Amazon S3, Amazon DynamoDB
- **Networking and delivery:** Amazon CloudFront, Amazon Route 53
- **API and communication:** Amazon API Gateway, Amazon SES
- **Security:** AWS IAM, AWS Certificate Manager
- **DevOps:** Git, GitHub, GitHub Actions, CI/CD
- **Frontend:** HTML, CSS and JavaScript

## Learning Outcomes

Through this project, I gained practical experience in:

- Designing a serverless cloud architecture.
- Hosting and delivering static website content using AWS.
- Connecting API Gateway endpoints to Python Lambda functions.
- Using DynamoDB for persistent application data.
- Integrating email functionality through Amazon SES.
- Configuring IAM permissions and HTTPS.
- Automating deployment using GitHub Actions.

## Future Improvements

- Expand automated testing for backend functions and API endpoints.
- Improve monitoring, logging and error handling.
- Review deployment security and operational cost optimisation.

## Author

Sraddha

GitHub: [sraddha444](https://github.com/sraddha444)
