# AWS General

## Benefits of cloud computing

- Elasticity
    - The ability to acquire resources as you need and release when they are no longer needed is termed as Elasticity of the Cloud.
    - With cloud computing, you don’t have to over-provision resources upfront to handle peak levels of business activity in the future. Instead, you provision the number of resources that you need. You can scale these resources up or down instantly to grow and shrink capacity as your business needs change.
- Reliability
    - Refers to the ability of a system to recover from infrastructure or service disruptions, by dynamically acquiring computing resources to meet demand, and mitigate disruptions.
    - Amazon VPC, AWS Trusted Advisor, AWS Service Quotas (formerly called AWS Service Limits).
- Durability
    - Refers to the ability of a system to assure data is stored and data remains consistently on the system as long as it is not changed by legitimate access, i.e. data should not get corrupt or disappear from the cloud because of a system malfunction.
- Resiliency
    - Describes the ability of a system to recover from a failure induced by the load (data or network), attacks, and failures (hardware, software, or network failures)

## Serverless Stack

AWS provides a set of fully managed services that you can use to build and run serverless applications.

- Serverless applications don’t require provisioning, maintaining, and administering servers for backend components such as compute, databases, storage, stream processing, message queueing, and more.
- You also no longer need to worry about ensuring application fault tolerance and availability.

Stack: Step Function, DynamoDB and Lambda

## Advantages of Cloud Computing

- Trade fixed expense for variable expense
    - Instead of having to invest heavily in data centers and servers before you know how you’re going to use them, you can pay only when you consume computing resources, and pay only for how much you consume.
- Benefit from massive economies of scale
    - By using cloud computing, you can achieve a lower variable cost than you can get on your own. Because usage from hundreds of thousands of customers is aggregated in the cloud, providers such as AWS can achieve higher economies of scale, which translates into lower pay as-you-go prices.
- Stop guessing capacity
    - Eliminate guessing on your infrastructure capacity needs. When you make a capacity decision prior to deploying an application, you often end up either sitting on expensive idle resources or dealing with limited capacity. With cloud computing, these problems go away. You can access as much or as little capacity as you need, and scale up and down as required with only a few minutes’ notice.
- Increase speed and agility
    - In a cloud computing environment, new IT resources are only a click away, which means that you reduce the time to make those resources available to your developers from weeks to just minutes. This results in a dramatic increase in agility for the organization, since the cost and time it takes to experiment and develop is significantly lower.
- Stop spending money running and maintaining data centers
    - Focus on projects that differentiate your business, not the infrastructure. Cloud computing lets you focus on your own customers, rather than on the heavy lifting of racking, stacking, and powering servers.
- Go global in minutes
    - Easily deploy your application in multiple regions around the world with just a few clicks. This means you can provide lower latency and a better experience for your customers at minimal cost.

## Inbound data transfer or data transfer between other AWS

There are three fundamental drivers of cost with AWS: compute, storage, and outbound data transfer.

In most cases, there is no charge for inbound data transfer or data transfer between other AWS services within the same region. Outbound data transfer is aggregated across services and then charged at the outbound data transfer rate.

Per AWS pricing, data transfer between S3 and EC2 instances within the same region is not charged, so there would be no data transfer charge for moving 500 GB of data from an EC2 instance to an S3 bucket in the same region.

## Region

Is a physical location around the world where AWS clusters data centers.

- Each AWS Region consists of multiple (two or more), isolated, and physically separate AZ's within a geographic area.
- Each AZ has independent power, cooling, and physical security and is connected via redundant, ultra-low-latency networks.

## Availability Zone

Is one or more discrete data centers with redundant power, networking, and connectivity in an AWS Region.

- All AZ’s in an AWS Region are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZ’s.

## Global Scope

Most of the services that AWS offers are Region specific. But few services, by definition, need to be in a global scope because of the underlying service they offer.

- AWS IAM
- Amazon CloudFront
- Route 53
- WAF

## Cloud Computing types

- Infrastructure as a Service (IaaS)
    - IaaS contains the basic building blocks for cloud IT. It typically provides access to networking features, computers (virtual or on dedicated hardware), and data storage space.
    - IaaS gives the highest level of flexibility and management control over IT resources.
    - Examples - Amazon EC2 (on AWS), GCP, Azure, Rackspace, Digital Ocean, Linode.
- Platform as a Service (PaaS)
    - PaaS removes the need to manage underlying infrastructure (usually hardware and operating systems) and allows you to focus on the deployment and management of your applications.
    - You don’t need to worry about resource procurement, capacity planning, software maintenance, patching, or any of the other undifferentiated heavy lifting involved in running your application.
    - Examples - Elastic Beanstalk (on AWS), Heroku, Google App Engine (GCP), Windows Azure (Microsoft).
- Software as a Service (SaaS)
    - SaaS provides you with a complete product that is run and managed by the service provider.
    - With a SaaS offering, you don’t have to think about how the service is maintained or how the underlying infrastructure is managed.
    - You only need to think about how you will use that particular software.
    - Examples - Amazon Rekognition, Google Apps (Gmail), Dropbox, Zoom.

---

# AWS CloudTrail

AWS CloudTrail is a service that enables governance, compliance, operational auditing, and risk auditing of your AWS account.

- CloudTrail provides an event history of your AWS account activity, including actions taken through the AWS Management Console, AWS SDKs, command-line tools, and other AWS services.
- CloudTrail can be used to record AWS API calls and other activity for your AWS account and save the recorded information to log files in an Amazon Simple Storage Service (Amazon S3) bucket that you choose.
- By default, the log files delivered by CloudTrail to your S3 bucket are encrypted using server-side encryption with Amazon S3–managed encryption keys (SSE-S3).

---

# Amazon Macie

Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect your sensitive data in AWS

- Macie automatically provides an inventory of Amazon S3 buckets including a list of unencrypted buckets, publicly accessible buckets, and buckets shared with AWS accounts outside those you have defined in AWS Organizations. Then, Macie applies machine learning and pattern matching techniques to the buckets you select to identify and alert you to sensitive data, such as personally identifiable information (PII).

---

# AWS Direct Connect

AWS Direct Connect is a cloud service solution that makes it easy to establish a dedicated network connection from your premises to AWS.

- You can use AWS Direct Connect to establish a private virtual interface from your on-premise network directly to your Amazon VPC, providing you with a private, high bandwidth network connection between your network and your VPC.
- This connection is private and does not go over the public internet.
- It takes at least a month to establish this physical connection.

---

# AWS Support

AWS offers three different support plans to cater to each of its customers:

- Basic
    - Customer Service & Communities - 24x7 access to customer service, documentation, whitepapers, and support forums.
    - AWS Trusted Advisor - Access to the 7 core Trusted Advisor checks and guidance to provision your resources following best practices to increase performance and improve security.
    - AWS Personal Health Dashboard - A personalized view of the health of AWS services, and alerts when your resources are impacted.
- Developer
    - AWS recommends Developer Support if you are testing or doing early development on AWS and want the ability to get email-based technical support during business hours as well as general architectural guidance as you build and test.
    - This plan provides access to just the 7 core Trusted Advisor checks.
- Business
    - AWS recommends Business Support if you have production workloads on AWS and want 24x7 phone, email and chat access to technical support and architectural guidance in the context of your specific use-cases.
    - You get full access to AWS Trusted Advisor Best Practice Checks.
    - You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components.
- Enterprise
    - AWS Enterprise Support provides customers with concierge-like service where the main focus is on helping the customer achieve their outcomes and find success in the cloud.
    - With Enterprise Support, you get access to online training with self-paced labs, 24x7 technical support from high-quality engineers, tools and technology to automatically manage the health of your environment, consultative architectural guidance, a designated Technical Account Manager (TAM) to coordinate access to proactive/preventative programs and AWS subject matter experts.
    - Provides customers with concierge-like service where the main focus is helping the customer achieve their outcomes and find success in the cloud.
    - You get access to guidance, configuration, and troubleshooting of AWS interoperability with many common operating systems, platforms, and application stack components.
    - Concierge
        - The Concierge Support Team are AWS billing and account experts that specialize in working with enterprise accounts.
        - They will quickly and efficiently assist you with your billing and account inquiries.

Obs: A basic support plan is included for all AWS customers.

---

# AWS Organizations


## Remove account from Organizations

You can remove an account from your organization only if the account has the information that is required for it to operate as a standalone account.
For each account that you want to make standalone, you must accept the AWS Customer Agreement, choose a support plan, provide and verify the required contact information, and provide a current payment method.
AWS uses the payment method to charge for any billable (not AWS Free Tier) AWS activity that occurs while the account isn't attached to an organization.

---

# AWS Software Developer Kit (SDK)

SDKs take the complexity out of coding by providing language-specific APIs for AWS services.

- For example, the AWS SDK for JavaScript simpliﬁes the use of AWS Services by providing a set of libraries that are consistent and familiar for JavaScript developers.
- It provides support for API lifecycle considerations such as credential management, retries, data marshaling, serialization, and deserialization.
- AWS SDKs are offered in several programming languages to make it simple for developers working on different programming and scripting languages.
- So, AWS SDK can help with using AWS services from within an application using language-specific APIs.

---

# AWS Simple Monthly Calculator

The Simple Monthly Calculator provides an estimate of usage charges for AWS services based on certain information you provide. It helps customers and prospects estimate their monthly AWS bill more efficiently.

- This calculator provides a visual interface to enter details about the AWS services that you plan to use and then it outputs a detailed estimate of the monthly AWS bill.

---

# VPC

Amazon Virtual Private Cloud (Amazon VPC) lets you provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define. You have complete control over your virtual networking environment, including the selection of your IP address range, creation of subnets, and configuration of route tables and network gateways.

## AWS services that allow VPC Endpoint Gateway

A VPC endpoint enables you to privately connect your VPC to supported AWS services and VPC endpoint services powered by AWS PrivateLink without requiring an internet gateway, NAT device, VPN connection, or AWS Direct Connect connection.

- Instances in your VPC do not require public IP addresses to communicate with resources in the service.
- Traffic between your VPC and the other service does not leave the Amazon network.
- There are two types of VPC endpoints:
    - interface endpoints
        - An interface endpoint is an elastic network interface with a private IP address from the IP address range of your subnet that serves as an entry point for traffic destined to a supported service.
        - Interface endpoints are powered by AWS PrivateLink, a technology that enables you to privately access services by using private IP addresses.
    - gateway endpoints
        - A gateway endpoint is a gateway that you specify as a target for a route in your route table for traffic destined to a supported AWS service.
        - The following AWS services are supported:
            - Amazon S3
            - DynamoDB

---

# Contact AWS Abuse Team

The AWS Trust & Safety team can assist you when AWS resources are used to engage in the following types of abusive behavior:

- Spam:
    - You are receiving unwanted emails from an AWS-owned IP address, or AWS resources are used to spam websites or forums.
- Port scanning:
    - Your logs show that one or more AWS-owned IP addresses are sending packets to multiple ports on your server. You also believe this is an attempt to discover unsecured ports.
- Denial-of-service (DoS) attacks:
    - Your logs show that one or more AWS-owned IP addresses are used to flood ports on your resources with packets. You also believe that this is an attempt to overwhelm or crash your - server or the software running on your server.
- Intrusion attempts:
    - Your logs show that one or more AWS-owned IP addresses are used to attempt to log in to your resources.
- Hosting prohibited content:
    - You have evidence that AWS resources are used to host or distribute prohibited content, such as illegal content or copyrighted content without the consent of the copyright holder.
- Distributing malware:
    - You have evidence that AWS resources are used to distribute software that was knowingly created to compromise or cause harm to computers or machines that it's installed on.

---

# EC2

## Amazon EC2 Instance Connect

Amazon EC2 Instance Connect provides a simple and secure way to connect to your Linux instances using Secure Shell (SSH).

- With EC2 Instance Connect, you use AWS Identity and Access Management (IAM) policies and principals to control SSH access to your instances, removing the need to share and manage SSH keys.
- Instance Connect will need port 22 to be open for traffic.

## Storage

Amazon EC2 provides you with flexible, cost effective, and easy-to-use data storage options for your instances. Each option has a unique combination of performance and durability. These storage options can be used independently or in combination to suit your requirements.

### Instance Store

An instance store provides temporary block-level storage for your instance.

- This storage is located on disks that are physically attached to the host computer.
- This is a good option when you need storage with very low latency, but you don't need the data to persist when the instance terminates or you can take advantage of fault-tolerant architectures.
- For this use-case, the computation application itself has a fault tolerant architecture, so it can automatically handle any failures of Instance Store volumes.

---

# AWS Step Function

Lets you coordinate multiple AWS services into serverless workflows.

- You can design and run workflows that stitch together services such as AWS Lambda, AWS Glue and Amazon SageMaker.

---

# Amazon DynamoDB

Is a key-value and document database that delivers single-digit millisecond performance at any scale.

- It's a fully managed, multi-Region, multi-master, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.

Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed to run high-performance applications at any scale.

- DynamoDB offers built-in security, continuous backups, automated multi-region replication, in-memory caching, and data export tools.
- DynamoDB global tables
    - Replicate data automatically across your choice of AWS Regions and automatically scale capacity to accommodate your workloads.
    - With global tables, your globally distributed applications can access data locally in the selected regions to get single-digit millisecond read and write performance.
    - DynamoDB offers active-active cross-region support.
        - Active-active clustering is a data resiliency architecture in which client workloads are distributed across two or more nodes in a cluster to keep your data safe and available in the event of an unexpected component failure.

---

# AWS Lambda

AWS Lambda lets you run code without provisioning or managing servers.

- You pay only for the compute time you consume.
- With Lambda, you can run code for virtually any type of application or backend service - all with zero administration.
- Just upload your code and Lambda takes care of everything required to run and scale your code with high availability.

---

# AWS Elastic Load Balancing

Elastic Load Balancing is used to automatically distribute your incoming application traffic across all the EC2 instances that you are running.

- You can use Elastic Load Balancing to manage incoming requests by optimally routing traffic so that no one instance is overwhelmed.
- Your load balancer acts as a single point of contact for all incoming web traffic to your application.
- When an instance is added, it needs to register with the load balancer or no traffic is routed to it.
- When an instance is removed, it must deregister from the load balancer or traffic continues to be routed to it.

---

# AWS Artifact

AWS Artifact is your go-to, central resource for compliance-related information that matters to your organization.

- It provides on-demand access to AWS’ security and compliance reports and select online agreements.
- Reports available in AWS Artifact include our Service Organization Control (SOC) reports, Payment Card Industry (PCI) reports, and certifications from accreditation bodies across geographies and compliance verticals that validate the implementation and operating effectiveness of AWS security controls.
- Different types of agreements are available in AWS Artifact Agreements to address the needs of customers subject to specific regulations.
- For example, the Business Associate Addendum (BAA) is available for customers that need to comply with the Health Insurance Portability and Accountability Act (HIPAA).
- It is not a service, it's a no-cost, self-service portal for on-demand access to AWS’ compliance reports.

---

# Redshift

Amazon Redshift is a fully-managed petabyte-scale cloud-based data warehouse product designed for large scale data set storage and analysis.

---

# Amazon EMR

Amazon EMR is the industry-leading cloud big data platform for processing vast amounts of data using open source tools such as Hadoop, Apache Spark, Apache Hive, Apache HBase, Apache Flink, Apache Hudi, and Presto.

- Amazon EMR can be used to provision resources to run big data workloads on Hadoop clusters.
- EMR provisions EC2 instances to manage its workload.

---

# AWS Elastic Beanstalk

Is an easy-to-use service for deploying and scaling web applications and services.

- You simply upload your code and Elastic Beanstalk automatically handles the deployment, from capacity provisioning, load balancing, auto-scaling to application health monitoring.

---

# AWS Shield

AWS Shield is a managed Distributed Denial of Service (DDoS) protection service that safeguards applications running on AWS.

- AWS Shield provides always-on detection and automatic inline mitigations that minimize application downtime and latency, so there is no need to engage AWS Support to benefit from DDoS protection.
- There are two tiers of AWS Shield - Standard and Advanced.

- Standard
    - AWS Shield Standard defends against most common, frequently occurring network and transport layer DDoS attacks that target your web site or applications.
    - When you use AWS Shield Standard with Amazon CloudFront and Amazon Route 53, you receive comprehensive availability protection against all known infrastructure (Layer 3 and 4) attacks.
    - All AWS customers benefit from the automatic protections of AWS Shield Standard, at no additional charge.
- Advanced
    - For higher levels of protection against attacks targeting your applications running on Amazon Elastic Compute Cloud (EC2), Elastic Load Balancing (ELB), Amazon CloudFront, AWS Global Accelerator and Amazon Route 53 resources, you can subscribe to AWS Shield Advanced.
    - AWS Shield Advanced includes intelligent DDoS attack detection and mitigation for not only for network layer (layer 3) and transport layer (layer 4) attacks but also for application layer (layer 7) attacks.
    - AWS Shield Advanced is a paid service that provides additional protections for internet-facing applications.
    - In addition to the network and transport layer protections that come with Standard, AWS Shield Advanced provides additional detection and mitigation against large and sophisticated DDoS attacks, near real-time visibility into attacks, and integration with AWS WAF, a web application firewall.

---

# AWS Web Application Firewall (AWS WAF)

AWS WAF is a web application firewall that helps protect web applications from attacks by allowing you to configure rules that allow, block, or monitor (count) web requests based on conditions that you define. These conditions include IP addresses, HTTP headers, HTTP body, URI strings, SQL injection, and cross-site scripting.

- Works with an Amazon CloudFront distribution, an Amazon API Gateway API, or an Application Load Balancer.
- AWS WAF charges based on the number of web access control lists (web ACLs) that you create, the number of rules that you add per web ACL, and the number of web requests that you receive
- HTTP and HTTPS requests are part of the Application layer, which is layer 7.
- You can use the IP address based match rule to block specific geographies, the accuracy of the IP Address to country lookup database varies by Region. Based on recent tests, AWS mentions that the overall accuracy for the IP address to country mapping is 99.8%.

---

# AWS Secrets Manager

AWS Secrets Manager helps you protect secrets needed to access your applications, services, and IT resources.

- The service enables you to easily rotate, manage, and retrieve database credentials, API keys, and other secrets throughout their lifecycle.
- With Secrets Manager, you pay based on the number of secrets stored and API calls made.

---

# AWS Partner Network

The AWS Partner Network (APN) is the global partner program for technology and consulting businesses that leverage Amazon Web Services to build solutions and services for customers.

- Consulting Partner
    - APN Consulting Partners are professional services firms that help customers of all types and sizes design, architect, build, migrate, and manage their workloads and applications on AWS, accelerating their migration to AWS cloud.
- Technology Partner
    - APN Technology Partners provide hardware, connectivity services, or software solutions that are either hosted on or integrated with, the AWS Cloud.

---

# AWS Trusted Advisor

AWS Trusted Advisor is an online tool that provides you real-time guidance to help you provision your resources following AWS best practices on cost optimization, security, fault tolerance, service limits, and performance improvement.

- Establishing new workflows, developing applications, or as part of ongoing improvement, recommendations provided by Trusted Advisor regularly help keep your solutions provisioned optimally.
- All AWS customers get access to the seven core Trusted Advisor checks to help increase the security and performance of the AWS environment. Trusted Advisor cannot be used to migrate to AWS and manage applications on AWS Cloud.

---

# Amazon CloudWatch

Amazon CloudWatch is a monitoring and observability service built for DevOps engineers, developers, site reliability engineers (SREs), and IT managers.

- CloudWatch provides data and actionable insights to monitor applications, respond to system-wide performance changes, optimize resource utilization, and get a unified view of operational health.

## CloudWatch Events

Rule that triggers on a schedule via a cron expression, you can then set the Lambda as the target for this rule.

## CloudWatch Billing Alarms

Sends an alarm when the actual cost exceeds a certain threshold.

---

# AWS Systems Manager

Gain operational insights into AWS and on-premises resources

- Improve visibility and control in the cloud, on premises, and at the edge.
- Shorten the time to detect and resolve operational issues.
- Maintain instance compliance against your patch, configuration, and custom policies.
- Automate configuration and ongoing management of your applications and resources.

---

# AWS KMS

AWS Key Management Service (KMS) makes it easy for you to create and manage cryptographic keys and control their use across a wide range of AWS services and in your applications.

- AWS KMS is a secure and resilient service that uses hardware security modules that have been validated under FIPS 140-2, or are in the process of being validated, to protect your keys.

---

# AWS Compute Optimizer

AWS Compute Optimizer helps you identify the optimal AWS resource configurations, such as Amazon EC2 instance types, Amazon EBS volume configurations, and AWS Lambda function memory sizes, using machine learning to analyze historical utilization metrics. AWS Compute Optimizer delivers recommendations for selected types of EC2 instances, EC2 Auto Scaling groups, EBS volumes, and Lambda functions.

- Compute Optimizer calculates an individual performance risk score for each resource dimension of the recommended instance, including CPU, memory, EBS throughput, EBS IOPS, disk throughput, disk throughput, network throughput, and network packets per second (PPS).
- AWS Compute Optimizer provides EC2 instance type and size recommendations for EC2 Auto Scaling groups with a fixed group size, meaning desired, minimum, and maximum are all set to the same value and have no scaling policy attached.
- AWS Compute Optimizer supports IOPS and throughput recommendations for General Purpose (SSD) (gp3) volumes and IOPS recommendations for Provisioned IOPS (io1 and io2) volumes.
- Compute Optimizer helps you optimize two categories of Lambda functions. The first category includes Lambda functions that may be over-provisioned in memory sizes. The second category includes compute-intensive Lambda functions that may benefit from additional CPU power.
- Over-provisioning resources can lead to unnecessary infrastructure costs, and under-provisioning resources can lead to poor application performance.
- Compute Optimizer recommends up to 3 options from 140+ EC2 instance types, as well as a wide range of EBS volume and Lambda function configuration options, to right-size your workloads.
- Compute Optimizer also projects what the CPU utilization, memory utilization, and run time of your workload would have been on recommended AWS resource options. This helps you understand how your workload would have performed on the recommended options before implementing the recommendations.

---

# AWS Budgets

AWS Budgets allows you to set custom budgets to track your cost and usage from the simplest to the most complex use cases.

- With AWS Budgets, you can choose to be alerted by email or SNS notification when actual or forecasted cost and usage exceed your budget threshold, or when your actual RI and Savings Plans' utilization or coverage drops below your desired threshold.
- With AWS Budget Actions, you can also configure specific actions to respond to cost and usage status in your accounts, so that if your cost or usage exceeds or is forecasted to exceed your threshold, actions can be executed automatically or with your approval to reduce unintentional over-spending.

---

# AWS Cost Explorer

AWS Cost Explorer has an easy-to-use interface that lets you visualize, understand, and manage your AWS costs and usage over time.

- Cost Explorer Resource Rightsizing Recommendations and Compute Optimizer use the same recommendation engine.
- The Compute Optimizer recommendation engine delivers recommendations to help customers identify optimal EC2 instance types for their workloads.
- The Cost Explorer console and API surface a subset of these recommendations that may lead to cost savings, and augments them with customer-specific cost and savings information (e.g. billing information, available credits, RI, and Savings Plans) to help Cost Management owners quickly identify savings opportunities through infrastructure rightsizing.
- Compute Optimizer console and its API delivers all recommendations regardless of the cost implications.

---

# Customer Managed CMK

A customer master key (CMK) is a logical representation of a master key.

- The CMK includes metadata, such as the key ID, creation date, description, and key state.
- The CMK also contains the key material used to encrypt and decrypt data. These are created and managed by the AWS customer. Access to these can be controlled using the AWS IAM service.

---

# Amazon Inspector

Amazon Inspector is an automated security assessment service that helps improve the security and compliance of applications deployed on your Amazon EC2 instances.

- Amazon Inspector automatically assesses applications for exposure, vulnerabilities, and deviations from best practices.
- After performing an assessment, Amazon Inspector produces a detailed list of security findings prioritized by level of severity. These findings can be reviewed directly or as part of detailed assessment reports which are available via the Amazon Inspector console or API.

---

# Amazon GuardDuty

Amazon GuardDuty is a threat detection service that monitors malicious activity and unauthorized behavior to protect your AWS account.

- GuardDuty analyzes billions of events across your AWS accounts from AWS CloudTrail (AWS user and API activity in your accounts), Amazon VPC Flow Logs (network traffic data), and DNS Logs (name query patterns).
- This service is for AWS account level access, not for instance-level management like an EC2.
- GuardDuty cannot be used to check OS vulnerabilities.

---

# Route 53

Amazon Route 53 is a highly available and scalable cloud Domain Name System (DNS) web service.

- It is designed to give developers and businesses an extremely reliable and cost-effective way to route end users to Internet applications by translating names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers use to connect to each other.

## Routing

- Simple routing policy
    - Use for a single resource that performs a given function for your domain, for example, a web server that serves content for the example.com website.
- Failover routing policy
    - Use when you want to configure active-passive failover.
- Geolocation routing policy
    - Use when you want to route traffic based on the location of your users.
- Geoproximity routing policy
    - Use when you want to route traffic based on the location of your resources and, optionally, shift traffic from resources in one location to resources in another.
- Latency routing policy
    - Use when you have resources in multiple AWS Regions and you want to route traffic to the Region that provides the best latency with less round-trip time.
- Multivalue answer routing policy
    - Use when you want Route 53 to respond to DNS queries with up to eight healthy records selected at random.
- Weighted routing policy
    - Use to route traffic to multiple resources in proportions that you specify.

---

# Amazon DocumentDB

Amazon DocumentDB (with MongoDB compatibility) is a fast, scalable, highly available, and fully managed document database service that supports MongoDB workloads.

- As a document database, Amazon DocumentDB makes it easy to store, query, and index JSON data.

---

# Amazon EFS

Amazon Elastic File System (Amazon EFS) provides a simple, scalable, fully managed elastic NFS file system for use with AWS Cloud services and on-premises resources.

- Is built to scale on-demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage capacity to accommodate growth.
- The service is designed to be highly scalable, highly available, and highly durable.
- Amazon EFS file systems store data and metadata across multiple Availability Zones in an AWS Region. EFS file system can be mounted on instances across multiple Availability Zones.

---

# Amazon SQS

Amazon Simple Queue Service (SQS) is a fully managed message queuing service that enables you to decouple and scale microservices, distributed systems, and serverless applications.

- Using SQS, you can send, store, and receive messages between software components at any volume, without losing messages or requiring other services to be available.

---

# Amazon SNS

Amazon Simple Notification Service (SNS) is a highly available, durable, secure, fully managed pub/sub messaging service that enables you to decouple microservices, distributed systems, and serverless applications.

- Using Amazon SNS topics, your publisher systems can fan-out messages to a large number of subscriber endpoints for parallel processing, including Amazon SQS queues, AWS Lambda functions, and HTTP/S webhooks.
- Additionally, SNS can be used to fan out notifications to end users using mobile push, SMS, and email.

---

# Amazon RDS

Amazon Relational Database Service (Amazon RDS) makes it easy to set up, operate, and scale a relational database in the cloud. It provides cost-efficient and resizable capacity while automating time-consuming administration tasks such as hardware provisioning, database setup, patching, and backups.

- Amazon RDS provides a selection of instance types optimized to fit different relational database use cases.
Instance types comprise varying combinations of CPU, memory, storage, and networking capacity and give you the flexibility to choose the appropriate mix of resources for your database to optimize the database for your use-case by selecting the correct instance type and size.
- As the RDS instances are optimized for memory, performance, or I/O, therefore the performance of AWS managed RDS instance is better than a customer-managed database instance.
- Multi-AZ DB Instance
    - When you provision a Multi-AZ DB Instance, Amazon RDS automatically creates a primary DB Instance and synchronously replicates the data to a standby instance in a different Availability Zone (AZ).
    - In case of an infrastructure failure, Amazon RDS performs an automatic failover to the standby (or to a read replica in the case of Amazon Aurora), so that you can resume database operations as soon as the failover is complete.
    - Since the endpoint for your DB Instance remains the same after a failover, your application can resume database operation without the need for manual administrative intervention.

---

# Amazon Transcribe

You can use Amazon Transcribe to add speech-to-text capability to your applications.

- Amazon Transcribe uses a deep learning process called automatic speech recognition (ASR) to convert speech to text quickly and accurately.
- Amazon Transcribe can be used to transcribe customer service calls, to automate closed captioning and subtitling, and to generate metadata for media assets.

---

# Amazon Polly

You can use Amazon Polly to turn text into lifelike speech thereby allowing you to create applications that talk.

- Polly's Text-to-Speech (TTS) service uses advanced deep learning technologies to synthesize natural sounding human speech.

---

# AWS X-Ray

You can use AWS X-Ray to analyze and debug serverless and distributed applications such as those built using a microservices architecture.

- With X-Ray, you can understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors.

---

# EC2

Amazon EC2 Spot Instances let you take advantage of unused EC2 capacity in the AWS cloud.

- Spot Instances are available at up to a 90% discount compared to On-Demand prices.
- You can use Spot Instances for various stateless, fault-tolerant, or flexible applications such as big data, containerized workloads, CI/CD, web servers, high-performance computing (HPC), and other test & development workloads.

---

# AWS CloudHSM

AWS CloudHSM is a cloud-based hardware security module (HSM) that enables you to easily generate and use your encryption keys on the AWS Cloud

- With CloudHSM, you can manage your encryption keys using FIPS 140-2 Level 3 validated HSMs.
- It is a fully-managed service that automates time-consuming administrative tasks for you, such as hardware provisioning, software patching, high-availability, and backups.

---

# Amazon S3

Object storage built to retrieve any amount of data from anywhere

- S3 One Zone-IA
    - Is for data that is accessed less frequently but requires rapid access when needed.
    - Unlike other S3 Storage Classes which store data in a minimum of three Availability Zones (AZs), S3 One Zone-IA stores data in a single AZ and costs 20% less than S3 Standard-IA.
    - S3 One Zone-IA offers the same high durability, high throughput, and low latency of S3 Standard, with a low per GB storage price and per GB retrieval fee.
    - Although S3 One Zone-IA offers less availability than S3 Standard.

---

# Amazon Athena

Amazon Athena is an interactive query service that makes it easy to analyze data in Amazon S3 using standard SQL.

- Athena is serverless, so there is no infrastructure to manage
- Pay only for the queries that you run.
- To use Athena, simply point to your data in Amazon S3, define the schema, and start querying using standard SQL. Most results are delivered within seconds.
- With Athena, there’s no need for complex ETL jobs to prepare your data for analysis. This makes it easy for anyone with SQL skills to quickly analyze large-scale datasets.

---

# Amazon Aurora

Is a MySQL and PostgreSQL-compatible relational database built for the cloud, that combines the performance and availability of traditional enterprise databases with the simplicity and cost-effectiveness of open source databases.

---

# AWS CloudFormation

Provides a common language to model and provision AWS and third-party application resources in your cloud environment.

- Allows you to use programming languages or a simple text file to model and provision, in an automated and secure manner, all the resources needed for your applications across all Regions and accounts.
- Think infrastructure as code; think CloudFormation.

---

# AWS Service Catalog

Allows organizations to create and manage catalogs of IT services that are approved for use on AWS.

- These IT services can include everything from virtual machine images, servers, software, and databases to complete multi-tier application architectures.

---

# AWS Marketplace

Is a digital catalog with thousands of software listings from independent software vendors that make it easy to find, test, buy, and deploy software that runs on AWS.

- Includes thousands of software listings from popular categories such as security, networking, storage, machine learning, IoT, business intelligence, database, and DevOps.
- You can use AWS Marketplace as a buyer (subscriber) or as a seller (provider), or both.
- Anyone with an AWS account can use AWS Marketplace as a consumer and can register to become a seller.

---

# AWS Storage Gateway

AWS Storage Gateway is a hybrid cloud storage service that connects your existing on-premises environments with the AWS Cloud.

- Customers use Storage Gateway to simplify storage management and reduce costs for key hybrid cloud storage use cases. These include moving tape backups to the cloud, reducing on-premises storage with cloud-backed file shares, providing low latency access to data in AWS for on-premises applications, as well as various migration, archiving, processing, and disaster recovery use cases.
- AWS Storage Gateway service provides three different types of gateways
    - Tape Gateway
    - File Gateway
    - Volume Gateway
    - That seamlessly connect on-premises applications to cloud storage, caching data locally for low-latency access.

---

# Amazon CloudFront

AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.

Amazon CloudFront is a fast content delivery network (CDN) service that securely delivers data, videos, applications, and APIs to customers globally with low latency, high transfer speeds, all within a developer-friendly environment.

---

# Amazon Rekognition

With Amazon Rekognition, you can identify objects, people, text, scenes, and activities in images and videos, as well as detect any inappropriate content.

- Amazon Rekognition also provides highly accurate facial analysis and facial search capabilities that you can use to detect, analyze, and compare faces for a wide variety of user verification, people counting, and public safety use cases.
- Features
    - Content moderation
    - Face compare and search
    - Face detection and analysis
    - Labels
    - Custom labels
    - Text detection
    - Celebrity recognition
    - Video segment detection
    - Personal Protective Equipment (PPE) detection

---

# AWS Identity and Access Management (IAM)

AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely. Using IAM, you can create and manage AWS users and groups, and use permissions to allow and deny their access to AWS resources.

- IAM enables security best practices by allowing you to grant unique security credentials to users and groups to specify which AWS service APIs and resources they can access. These features make IAM an important service for the overall security of AWS resources in your account. IAM is secure by default; users have no access to AWS resources until permissions are explicitly granted.

- IAM User
    - Access keys are only tied to the IAM user
    - Access keys are long-term credentials for an IAM user or the AWS account root user.
    - You can use access keys to sign programmatic requests to the AWS CLI or AWS API (directly or using the AWS SDK).
    - Access keys consist of two parts: an access key ID (for example, AKIAIOSFODNN7EXAMPLE) and a secret access key (for example, wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY).
    - As a user name and password, you must use both the access key ID and secret access key together to authenticate your requests.
- IAM Role
    - An IAM role is similar to an IAM user, in that it is an AWS identity with permission policies that determine what the identity can and cannot do in AWS.
    - However, instead of being uniquely associated with one person, a role is intended to be assumable by anyone who needs it.
- IAM Group
    - An IAM group is a collection of IAM users.
    - Groups let you specify permissions for multiple users, which can make it easier to manage the permissions for those users.

---

# Amazon Elastic Container Registry (ECR)

Amazon Elastic Container Registry (ECR) can be used to store, manage, and deploy Docker container images.

- Eliminates the need to operate your container repositories.
- You can then pull your docker images from ECR and run those on Amazon Elastic Container Service (ECS).

---

# Amazon Elastic Container Service (ECS)

Amazon Elastic Container Service (Amazon ECS) is a highly scalable, fast, container management service that makes it easy to run, stop, and manage Docker containers on a cluster.

- You cannot use ECS to store and deploy docker container images.

## Fargate launch type

AWS Fargate is a serverless compute engine for containers. It works with both Amazon Elastic Container Service (ECS) and Amazon Elastic Kubernetes Service (EKS).

- Fargate makes it easy for you to focus on building your applications.
- Fargate removes the need to provision and manage servers, lets you specify and pay for resources per application, and improves security through application isolation by design.
- Fargate allocates the right amount of compute, eliminating the need to choose instances and scale cluster capacity.
- You only pay for the resources required to run your containers, so there is no over-provisioning and paying for additional servers.
- Fargate runs each task or pod in its kernel providing the tasks and pods their own isolated compute environment. This enables your application to have workload isolation and improved security by design.

---

# AWS Service Health Dashboard

AWS Service Health Dashboard publishes most up-to-the-minute information on the status and availability of all AWS services in tabular form for all Regions that AWS is present in.

- You can check on this page https://status.aws.amazon.com/ to get current status information.

---

# AWS Personal Health Dashboard

AWS Personal Health Dashboard provides alerts and remediation guidance when AWS is experiencing events that may impact you.

- While the Service Health Dashboard displays the general status of AWS services, Personal Health Dashboard gives you a personalized view of the performance and availability of the AWS services underlying your AWS resources.

---

# AWS Systems Manager Session Manager

AWS SSM Session Manager is a fully-managed service that provides you with an interactive browser-based shell and CLI experience. It helps provide secure and auditable instance management without the need to open inbound ports, maintain bastion hosts, and manage SSH keys.

- Session Manager helps to enable compliance with corporate policies that require controlled access to instances, increase security and auditability of access to the instances while providing simplicity and cross-platform instance access to end-users.

---

# AWS Service Quotas

Service Quotas enables you to view and manage your quotas for AWS services from a central location.

- Quotas, also referred to as limits in AWS, are the maximum values for the resources, actions, and items in your AWS account.
- Each AWS service defines its quotas and establishes default values for those quotas.

---

# AWS VPN

AWS Virtual Private Network (VPN) solutions establish secure connections between on-premises networks, remote offices, client devices, and the AWS global network.

- AWS VPN is comprised of two services: AWS Site-to-Site VPN and AWS Client VPN. Together, they deliver a highly-available, managed, and elastic cloud VPN solution to protect your network traffic.

---

# Amazon FSx for Windows File Server

Amazon FSx for Windows File Server provides fully managed, highly reliable, and scalable file storage that is accessible over the industry-standard Service Message Block (SMB) protocol. It is built on Windows Server, delivering a wide range of administrative features such as user quotas, end-user file restore, and Microsoft Active Directory (AD) integration.

- To support a wide spectrum of workloads, Amazon FSx provides high levels of throughput, IOPS and consistent sub-millisecond latencies.
- Amazon FSx is accessible from Windows, Linux, and macOS compute instances and devices.
- For Windows-based applications, Amazon FSx provides fully managed Windows file servers with features and performance optimized for "lift-and-shift" business-critical application workloads including home directories (user shares), media workflows, and ERP applications. It is accessible from Windows and Linux instances via the SMB protocol.

---

# Amazon FSx for Lustre

For compute-intensive and fast processing workloads, like high-performance computing (HPC), machine learning, EDA, and media processing, Amazon FSx for Lustre, provides a file system that’s optimized for performance, with input and output stored on Amazon S3.

- FSx for Lustre is only compatible with Linux.

---

# Global Accelerator

AWS Global Accelerator is a service that improves the availability and performance of your applications with local or global users. It provides static IP addresses that act as a fixed entry point to your application endpoints in a single or multiple AWS Regions, such as your Application Load Balancers, Network Load Balancers, or Amazon EC2 instances. 

- AWS Global Accelerator uses the AWS global network to optimize the path from your users to your applications, improving the performance of your traffic by as much as 60%.
- Global Accelerator improves performance for a wide range of applications over TCP or UDP by proxying packets at the edge to applications running in one or more AWS Regions. 
- Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP, as well as for HTTP use cases that specifically require static IP addresses or deterministic, fast regional failover.

---

# AWS Auto Scaling

AWS Auto Scaling monitors applications and automatically adjusts capacity to maintain steady, predictable performance at the lowest possible cost.

- Using AWS Auto Scaling, it’s easy to setup application scaling for multiple resources across multiple services in minutes.
- The service provides a simple, powerful user interface that lets you build scaling plans for resources including Amazon EC2 instances and Spot Fleets, Amazon ECS tasks, Amazon DynamoDB tables and indexes, and Amazon Aurora Replicas.
- AWS Auto Scaling makes scaling simple with recommendations that allow you to optimize performance, costs, or balance between them.

---

# AWS Local Zones

AWS Local Zones allow you to use select AWS services, like compute and storage services, closer to more end-users, providing them very low latency access to the applications running locally.

- AWS Local Zones are also connected to the parent region via Amazon’s redundant and very high bandwidth private network, giving applications running in AWS Local Zones fast, secure, and seamless access to the rest of AWS services.
- You should use AWS Local Zones to deploy workloads closer to your end-users for low-latency requirements.
- AWS Local Zones have their connection to the internet and support AWS Direct Connect, so resources created in the Local Zone can serve local end-users with very low-latency communications.
- Various AWS services such as Amazon Elastic Compute Cloud (EC2), Amazon Virtual Private Cloud (VPC), Amazon Elastic Block Store (EBS), Amazon FSx, Amazon Elastic Load Balancing, Amazon EMR, Amazon ElastiCache, and Amazon Relational Database Service (RDS) are available locally in the AWS Local Zones. You can also use services that orchestrate or work with local services such as Amazon EC2 Auto Scaling, Amazon EKS clusters, Amazon ECS clusters, Amazon EC2 Systems Manager, Amazon CloudWatch, AWS CloudTrail, and AWS CloudFormation.
- AWS Local Zones also provide a high-bandwidth, secure connection to the AWS Region, allowing you to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

---

# AWS Wavelength

AWS Wavelength extends the AWS cloud to a global network of 5G edge locations to enable developers to innovate and build a whole new class of applications that require ultra-low latency.

- Wavelength Zones provide a high-bandwidth, secure connection to the parent AWS Region, allowing developers to seamlessly connect to the full range of services in the AWS Region through the same APIs and toolsets.

---

# AWS Batch

You can use AWS Batch to plan, schedule and execute your batch computing workloads across the full range of AWS compute services.

- AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory optimized instances) based on the volume and specific resource requirements of the batch jobs submitted.
- AWS Batch provisions compute resources and optimizes the job distribution based on the volume and resource requirements of the submitted batch jobs.

---

# Amazon MQ

Amazon MQ is a managed message broker service for Apache ActiveMQ and RabbitMQ that makes it easy to set up and operate message brokers on AWS.

- Amazon MQ reduces your operational responsibilities by managing the provisioning, setup, and maintenance of message brokers for you.
- Because Amazon MQ connects to your current applications with industry-standard APIs and protocols, you can easily migrate to AWS without having to rewrite code.
- If you're using messaging with existing applications, and want to move the messaging functionality to the cloud quickly and easily, AWS recommends you consider Amazon MQ. It supports industry-standard APIs and protocols so you can switch from any standards-based message broker to Amazon MQ without rewriting the messaging code in your applications. 
- If you are building brand new applications in the cloud, AWS recommends you consider Amazon SQS and Amazon SNS.

---

# AWS Acceptable Use Policy

The Acceptable Use Policy describes prohibited uses of the web services offered by Amazon Web Services, Inc. and its affiliates (the “Services”) and the website located at http://aws.amazon.com (the “AWS Site”).

- This policy is present at https://aws.amazon.com/aup/ and is updated on a need basis by AWS.
