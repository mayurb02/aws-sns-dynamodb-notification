# Serverless Notification System – SNS & DynamoDB

## Overview
Built an event-driven notification pipeline where application events are 
published to an SNS Topic triggering real-time email/SMS notifications 
and logging all events to a DynamoDB table. Demonstrates pub/sub 
architecture patterns used in real-world microservices.

## AWS Services Used
`SNS` `DynamoDB` `IAM` `EC2` `CloudWatch` `Python` `Boto3`

## Architecture
- SNS Standard Topic for fan-out messaging to multiple subscribers
- Email and SMS subscriptions on SNS Topic for real-time alert delivery
- DynamoDB table (On-Demand mode) to log all events with timestamp and type
- IAM Role with least-privilege sns:Publish and dynamodb:PutItem permissions
- Python Boto3 script on EC2 to simulate event publishing to SNS and DynamoDB
- CloudWatch alarms on DynamoDB read/write capacity for health monitoring
- SNS Topic Policy restricting publishers to authorized IAM roles only

## Key Achievements
- Built fully event-driven architecture — zero manual intervention after trigger
- DynamoDB table designed with partition key (eventId) and sort key (timestamp)
- Restricted SNS publish rights to authorized IAM roles only — unauthorized access blocked
- CloudWatch alarms configured for DynamoDB capacity monitoring and alerts

## Skills Demonstrated
Event-Driven Architecture | Pub/Sub Messaging | NoSQL Database | 
Python Boto3 | IAM Security | CloudWatch Monitoring | Serverless Patterns
