## AWS: API, Dynamo and Lambda

### AWS API Gateway Overview

1. What is Amazon API Gateway?

   Amazon API Gateway is a managed service that allows developers to define the HTTP endpoints of a REST API or a WebSocket API and connect those endpoints with the corresponding backend business logic. It also handles authentication, access control, monitoring, and tracing of API requests.

2. Why is Amazon API Gateway an important part of the Serverless ecosystem?

   Many Serverless applications use Amazon API Gateway, which conveniently replaces the API servers with a managed serverless solution.

3. How does API Gateway integrate with other AWS services?

   API Gateway sits between the backend services of your API and your API’s users, handling the HTTP requests to your API endpoints and routing them to the correct backends. It provides a set of tools that help you manage your API definitions and the mappings between endpoints and their respective backend services. It can also generate API references from your definitions and make them available to your users as API documentation.

   API Gateway integrates with many other AWS services like AWS Lambda, AWS SNS, AWS IAM, and Cognito Identity Pools. These integrations allow for fully managed authentication and authorization layers, as well as detailed metrics and tracing for API requests.

---

### AWS API Gateway

1. What are the some benefits of using Amazon API Gateway?

   - Easy creation of RESTful APIs.
   - Scalability to handle varying workloads.
   - Secure API access and authorization.
   - Built-in caching for improved performance.
   - Seamless integration with AWS services.

2. What two API types might you choose from?
   1. REST APIs.
   2. WebSocket APIs for real-time, two-way communication.

---

### AWS DynamoDB Guide

1. What is DynamoDB?

   Amazon DynamoDB is a fully managed NoSQL database service provided by AWS. It offers reliable performance, seamless scalability, and automatic replication across multiple regions, making it ideal for applications with high read and write requirements.

2. Under what circumstances would you recommend DynamoDB over MongoDB?

   Applications with large amounts of data and strict latency requirements. As your amount of data scales, JOINs and advanced SQL operations can slow down your queries. With DynamoDB, your queries have predictable latency up to any size, including over 100 TBs!

   Serverless applications using AWS Lambda. AWS Lambda provides auto-scaling, stateless, ephemeral compute in response to event triggers. DynamoDB is accessible via an HTTP API and performs authentication & authorization via IAM roles, making it a perfect fit for building Serverless applications.

   Data sets with simple, known access patterns. If you're generating recommendations and serving them to users, DynamoDB's simple key-value access patterns make it a fast, reliable choice.

---

### AWS DynamoDB

1. Explain to a non-technical friend how DynamoDB works.
   DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale. DynamoDB offers built-in security, continuous backups, automated multi-Region replication, in-memory caching, and data export tools.

---

### Dynamoose

1. What is Dynamoose?

   Dynamoose is a modeling tool for Amazon's DynamoDB. Dynamoose is heavily inspired by Mongoose, which means if you are coming from Mongoose the syntax will be very familar.

2. What are some key features of Dynamoose?

   Type safety High level API Easy to use syntax Ability to transform data before saving or retrieving documents Strict data modeling (validation, required attributes, and more) Support for DynamoDB Transactions Powerful Conditional/Filtering Support Callback and Promise support.
