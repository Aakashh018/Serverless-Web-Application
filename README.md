# Serverless Web Application

This repository contains the source code and configuration for a serverless web application. The application is hosted on AWS using a combination of S3, CloudFront, Route 53, Lambda functions, and API Gateway, with SSL/TLS security provided by AWS Certificate Manager.

## Architecture Overview

1. *Domain and DNS Management*
   - *Domain*: Managed via Route 53.
   - *DNS Configuration*: Points to a CloudFront distribution.

2. *Content Delivery*
   - *CloudFront*: Distributes the static content (HTML, CSS, JavaScript) to users.
   - *S3 Bucket*: Stores the static files (HTML, CSS, JS) for the web application.
     - Direct access to the S3 bucket is restricted; users can only access files through CloudFront.

3. *Backend API*
   - *Lambda Functions*: Handles the backend operations.
     - *Insert Data*: Lambda function for inserting data into the database.
     - *Obtain Data*: Lambda function for retrieving data from the database.
   - *API Gateway*: Exposes the Lambda functions via RESTful endpoints.

4. *Security*
   - *SSL/TLS*:Implemented SSL/TLS certificates accross CloudFront ensuring compliance with modern security standards.
     
   - *Amazon Certificate Manager(ACM)*:Configured HTTPS using (ACM) to secure data transmission and Protect from data Leaks



![Blank diagram (3)](https://github.com/user-attachments/assets/09fc20f1-d876-4573-9239-93007aed01d9)
