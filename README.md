
# AWS Serverless Cloud Portfolio

## Project Overview

A personal portfolio website designed and deployed using Amazon Web Services (AWS). This project demonstrates practical experience with cloud hosting, serverless architecture, API integration, database operations, security and automated deployment.

## Architecture

The project uses AWS managed and serverless services to host the website and support backend functionality.

- **Amazon S3** – Stores the static website files.
- **Amazon CloudFront** – Distributes website content globally.
- **AWS Certificate Manager (ACM)** – Provides the SSL/TLS certificate for HTTPS.
- **Amazon Route 53** – Manages DNS for the custom domain.
- **Amazon API Gateway** – Exposes API endpoints for backend functionality.
- **AWS Lambda** – Runs Python functions to process requests.
- **Amazon DynamoDB** – Stores visitor-counter data.
- **Amazon SES** – Sends contact-form messages by email.
- **AWS IAM** – Controls access to AWS resources.
- **GitHub Actions** – Automates website deployment to Amazon S3 and CloudFront cache invalidation.

## Key Features

### 1. Static Website Hosting

Hosted the portfolio website using Amazon S3 and Amazon CloudFront, with HTTPS configured through AWS Certificate Manager and a custom domain managed through Route 53.

### 2. Serverless Visitor Counter

Implemented a visitor-counter API using Amazon API Gateway, an AWS Lambda function written in Python and Amazon DynamoDB to maintain persistent visitor-count data.

### 3. Contact Form

Integrated a contact form with Amazon API Gateway, AWS Lambda and Amazon SES to process submissions and send email notifications.

### 4. Automated Deployment

Configured a GitHub Actions workflow to automate website deployment to Amazon S3 and request CloudFront cache invalidation following updates.

### 5. Security

Used AWS IAM permissions to control access between services and applied least-privilege principles where appropriate. AWS credentials for the deployment workflow are configured through GitHub Actions secrets.

## CI/CD with GitHub Actions

The deployment workflow is defined in `.github/workflows/deploy.yml`.

### Workflow Trigger

The workflow runs whenever code is pushed to the `master` branch.

### Deployment Process

1. Checks out the repository using `actions/checkout`.
2. Configures AWS credentials using GitHub Actions secrets.
3. Synchronises website files with the configured Amazon S3 bucket using the AWS CLI.
4. Excludes Git metadata and GitHub workflow files from deployment.
5. Uses the `--delete` option to remove destination files that no longer exist in the source.
6. Requests CloudFront cache invalidation for all paths (`/*`) so updated content can be served.

### GitHub Actions Secrets

The workflow uses the following secrets for deployment configuration:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION`
- `S3_BUCKET_NAME`
- `CLOUDFRONT_DISTRIBUTION_ID`

Sensitive credentials are stored in GitHub Actions secrets rather than hard-coded in the workflow file.

### Benefits

- Automates deployment when changes are pushed to the repository.
- Reduces manual steps required to publish website updates.
- Synchronises website files with the configured S3 bucket.
- Requests CloudFront cache invalidation after deployment.

## Technologies Used

- **Cloud:** Amazon Web Services (AWS)
- **Compute:** AWS Lambda, Python
- **Storage and Database:** Amazon S3, Amazon DynamoDB
- **Content Delivery and DNS:** Amazon CloudFront, Amazon Route 53
- **API and Communication:** Amazon API Gateway, Amazon SES
- **Security:** AWS IAM, AWS Certificate Manager
- **DevOps:** Git, GitHub, GitHub Actions, CI/CD
- **Frontend:** HTML, CSS, JavaScript

## Learning Outcomes

Through this project, I gained practical experience in:

- Designing and deploying a serverless cloud architecture.
- Hosting and distributing static website content using AWS.
- Integrating API Gateway with Python-based Lambda functions.
- Using DynamoDB for persistent application data.
- Integrating email functionality through Amazon SES.
- Configuring HTTPS and IAM permissions.
- Automating website deployment using GitHub Actions.
- Understanding how AWS services work together to deliver a web application.

## Future Improvements

- Expand automated testing for backend functions and API endpoints.
- Improve monitoring, logging and error handling.
- Review deployment security and operational cost optimisation.

## Author

**Sraddha**

GitHub: [sraddha444](https://github.com/sraddha444)

Portfolio repository: [AWS Serverless Cloud Portfolio](https://github.com/sraddha444/portfolio_website)
