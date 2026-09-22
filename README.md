# AWS Serverless Web Application 🚀

A production-style serverless web application built using AWS services including **Amazon S3, CloudFront, API Gateway, Lambda, DynamoDB, IAM, and CloudWatch**.

The application provides a static web frontend through CloudFront and allows users to send data through an API Gateway endpoint. AWS Lambda processes the request and stores the data in DynamoDB.

---

## 🏗️ Architecture

```text
                         User Browser
                              |
              +---------------+---------------+
              |                               |
              v                               v
       Amazon CloudFront                API Gateway
              |                         POST /data
              v                               |
       Private Amazon S3                     v
        index.html                       AWS Lambda
                                              |
                                              v
                                        Amazon DynamoDB

                                      CloudWatch
                                      /       \
                                   Logs       Alarm
