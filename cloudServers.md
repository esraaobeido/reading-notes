# AWS: Cloud Servers

## AWS EC2
**1. What is an EC2 Instance?**
- An EC2 (Elastic Compute Cloud) instance is a virtual server provided by Amazon Web Services (AWS).
- It is a fundamental building block of cloud computing on AWS and allows users to run applications and services on the AWS infrastructure.

**2. Name 2 use cases for EC2.**
- Run cloud-native and enterprise applications. 
- Train and deploy ML applications.

**3. Provide 1 reason to use ECS instead of a service such as Heroku, Digital Ocean, or Render.com.**
- AWS is perfect for medium and large businesses. It should be chosen when one needs flexibility right from the initial application deployment.

---
## EC2 For Humans
**1. Where can we find EC2 on the AWS Console?**
To connect to your instance using the browser-based client from the Amazon EC2 console:

- Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/. 
- In the navigation pane, choose Instances. 
- Select the instance and choose Connect. 
- Choose EC2 Instance Connect. 
- Verify the user name and choose Connect to open a terminal window.

**2.Explain the general difference between T2 Micro and XL.**

- T2 instances are a low-cost, general purpose instance type that provides a baseline level of CPU performance with the ability to burst above the baseline when needed.

- X1 Instances are a part of the Amazon EC2 memory-optimized instance family and are designed for running large-scale and in-memory applications in the AWS Cloud.

**3. Explain a “Compute Cycle” to a non-technical friend.**
- A compute cycle is simply a small step in a larger task that a computer performs by taking data, processing it, and producing a result. The more compute cycles a computer can perform per second, the faster it can complete tasks.

---
## Elastic Beanstalk

**1. What is Elastic Beanstalk?**
- Elastic Beanstalk is an easy-to-use service that deploys managesand scales web apps and sevices for you.

**2. Describe the relationship between EC2 and Elastic Beanstalk.**
- Relationship Between EC2 and Elastic Beanstalk Elastic Beanstalk is one layer of abstraction away from the EC2 layer. 
Elastic Beanstalk will setup an “environment” for you that can contain a number of EC2 instances, an optional database, as well as a few other AWS components such as a Elastic Load Balancer, Auto-Scaling Group, Security Group.

**3. Name some benefits of using Elastic Beanstalk.**
- Timesaving server configuration. 
- Powerful customization. 
- Cost-effective price point.

