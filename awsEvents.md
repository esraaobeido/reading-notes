# AWS :Events

## AWS SQS vs SNS

### 1.What is the difference betweeen SQS and SNS?
SQS is a message queue service for decoupling components, while SNS is a pub/sub service for broadcasting messages to multiple subscribers. SQS uses point-to-point communication, whereas SNS follows a publish/subscribe model. SQS retains messages in the queue, while SNS doesn’t retain messages.

### 2.What are some use cases for both SNS and SQS?
Some cases for SNS:
- Sending notifications: SNS is ideal for broadcasting messages, such as sending out email notifications, SMS alerts, or push notifications to mobile devices.
- Fan-out architecture: It is suitable for scenarios where one message needs to be sent to multiple recipients, such as updating multiple databases or triggering multiple downstream processes.

Some cases for SQS:
- Decoupling components: SQS is used to create a loosely coupled architecture where components can interact without direct integration, reducing the risk of failure between systems.
- Load leveling: It helps in managing uneven message consumption rates, ensuring that the receiver can process messages at its own pace without overwhelming it.
- Task processing: SQS can be used for managing tasks and work items, ensuring they are processed efficiently by different workers or instances.

_ _ _

## AWS SNS and SQS

### 1. Describe how to use SQS and SNS in a “fanout” pattern.

For example, you can develop an application that publishes a message to an SNS topic whenever an order is placed for a product. Then, SQS queues that are subscribed to the SNS topic receive identical notifications for the new order. An Amazon Elastic Compute Cloud (Amazon EC2) server instance attached to one of the SQS queues can handle the processing or fulfillment of the order. And you can attach another Amazon EC2 server instance to a data warehouse for analysis of all orders received.

You can also use fanout to replicate data sent to your production environment with your test environment. Expanding upon the previous example, you can subscribe another SQS queue to the same SNS topic for new incoming orders. Then, by attaching this new SQS queue to your test environment, you can continue to improve and test your application using data received from your production environment.

### 2.Explain how “push notifications” work, using SNS.

Amazon SNS enables real-time push notifications to mobile devices (iOS, Android) and other endpoints (email, SMS). Users subscribe to SNS topics for specific updates. When a message is published to a topic, SNS delivers it to all subscribed devices, ensuring instant delivery of notifications.
_ _ _

## SQS and SNS Basics

### 1. How might a large scale, distributed application make use of a Queue system like SQS?

Decoupling Components: SQS allows different components of the application to communicate with each other indirectly through the queues. Instead of components directly calling each other's APIs, they can send messages to SQS queues, and other components can consume these messages at their own pace. This decoupling enables better isolation, flexibility, and fault tolerance.

Load Balancing: When a component of the distributed application receives a high volume of requests, it can use an SQS queue to offload the excess tasks. Other instances of the component can then consume messages from the queue, distributing the load and preventing overload on any single instance.

Asynchronous Processing: Certain tasks within a distributed application may be time-consuming or resource-intensive. By using SQS, these tasks can be performed asynchronously. Components can send tasks to an SQS queue, and separate worker processes can consume messages from the queue to process the tasks independently, allowing the application to continue serving other requests without waiting for the results.

-----