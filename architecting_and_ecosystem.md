# Well architected framework 5 pillars

## Operational Excellence

Includes the ability to run and monitor systems to deliver business value and to continually improve supporting processes and procedures

### Design Principles

- Perform operations as code
    - Infraestructure as code

- Annotate documentation
    - Automate the creation of annotated documentation after every build

- Make frequent, small, reversible changes
    - So that in case of any failure, you can reverse it

- Refine operatios procedures frequently
    - And ensure that team members are familiar with it

- Anticipate failure

- Learn rom all operational failures

### Services

- Prepare
    - AWS CloudFormation
    - AWS Config

- Operate
    - AWS CloudFormation
    - AWS Config
    - AWS CloudTrail
    - Amazon CloudWatch
    - AWS X-Ray

- Evolve
    - AWS CloudFormation
    - AWS CodeBuild
    - AWS CodeCommit
    - AWS CodeDeploy
    - AWS CodePipeline

## Security

Includes the ability to protect information, systes and assets while delivering business value through risk assessments and mitigation strategies

### Design Principles

- Implement a strong identity foundation
    - Centralize privilege management and reduce (or even eliminate) reliance on long-term credentials, Principle of least privilege - IAM

- Enable traceability
    - Integrate logs and metrics with systems to automatically respond and take action

- Apply security at all layers
    - Like edge network, VPC, subnet, load balancer, every instance, operating system and application

- Automate security best practices

- Protect data in transt and at rest
    - Encryption, tokenization and access control

- Keep people away from data
    - Reduce or eliminate the ned for direct access ormanual processing of data

- Prepare for security events
    - Run incident response simulatons and use tools with automation to increase your speed for detection, investigation and recovery

### Services

- Identity and Access Management
    - IAM
    - AWS-STS
    - MFA Token
    - AWS Organizations

- Detective Controls
    - AWS Config
    - AWS CloudTrail
    - Amazon CloudWatch

- Infraestructure Protection
    - Amazon CloudFront
    - Amazon VPC
    - AWS Shield
    - AWS WAF
    - Amazon Inspector

- Data Protection
    - KMS
    - S3
    - Elastic Load Balancing (ELB)
    - Amazon EBS
    - Amazon RDS

- Incident Response
    - IAM
    - AWS CloudFormation
    - Amazon Cloudwatch Events

## Reliability

Ability of a system to recover from infraestructure or service disruptions, dynamically acquire computing resources to meet demand, and mitigate disruptions such as misconfigurations or transient network issues

### Design Principles

- Test recovery procedures
    - Use automation to simulate different failures or to recreate scenarios that led failures before

- Automatically recover from failure
    - Antcipate an remediate failures before they occur

- Scale horizontally to increase aggregatee system availability
    - Distribute requests across muiltiple, smaller resources to ensure that they don't share a common point of failure

- Stop guessing capacity
    - Maintain the optimal level to satisfy demand without over or under provisioning, use Auto Scaling

- Manage changes in automation
    - Use automation to make changes to infraestructure

### Services

- Foundations
    - IAM
    - Amazon VPC
    - Service Quotas
    - AWS Trusted Advisor

- Change Management
    - AWS Auto Scaling
    - Amazon CloudWatch
    - AWS CloudTrail
    - AWS Config

- Failures
    - Backups
    - AWS CloudFormation
    - Amazon S3
    - Amazon S3 Glacier
    - Amazon Route 53

## Performance Efficiency

Includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve

### Design Principles

- Democratize advanced technologies
    - Advance technologies become services and hence you can focus more on prodct development

- Go global in minutes
    - Easy deployment in multiple regions

- Use serverless architectures
    - Avoid burden of managing servers

- Experiment more often
    - Easy to carry out comparative testing

- Mechanical sympathy
    - Be aware of all AWS services

### Services

- Selection
    - AWS Auto Scaling
    - AWS Lambda
    - Amazon Elastic Block Store (EBS)
    - Amazon RDS

- Review
    - AWS CloudFormation
    - AWS News Blog

- Monitoring
    - Amazon CloudWatch
    - AWS Lambda

- Tradeoffs
    - Amazon RDS
    - Amazon ElastiCache
    - AWS Snowball
    - Amazon CloudFront

## Cost Optmization

Includes the ability to run systems to deliver business value at the lowest price point

### Desing Principles

- Adopt a consumption mode
    - Pay only for what you use

- Measure overall efficiency
    - Use CloudWatch

- Stop spending money on data center operations
    - AWS does the infraestructure part and enables customer to focus on organization projects

- Analyze and attribute expenditure
    - Accurate indentification of system usage and costs, helps measure return on investment (ROI), make sure to use tags

- Use managed and application level services to reduce of ownership
    - As managed services operate at cloud, they can offer a lower cost per transaction or service

### Services

- Expenditure Awareness
    - AWS Budgets
    - AWS Cost and Usage Report
    - AWS Cost Explorer
    - Reserved Instance Reporting

- Cost-Effective Resources
    - Spot Instance
    - Reserved Instance
    - Amazon S3 Glacier

- Matching supply and demand
    - AWS Auto Scaling
    - AWS Lambda

- Optimizing Over Time
    - AWS Trusted Advisor
    - AWS Cost and Usage Report
    - AWS News Blog



# AWS Well-Architected Tool

Free tool to review your architectures against the 5 pillars Well-Architectured Framework and adopt architectural best practives

## How it works

- Select your workload and answer questions
- Review your answers against the 5 pillars
- Obtain advice: get videos and documentations, generate a report, see the results in a dashboard



# AWS Right Sizing

- EC2 has many instance types, but choosing the most powerful instance type isn't best choice, because the cloud is elastic
- Right sizing is the process of matching instance types andd sizes o your workload performance and capacity requirements at the lowest possible cost
- Scaling up is easy so start small
- It's also the process of looking at deployed instances and indentifying opportunities to eliminate or downsize without compromising capacity or other requirements, wich results in lower costs
- It's important to Right Size...
    - Before a Cloud Migration
    - Continuously after the cloud onboarding process (requirements change over time)
- To make a right size use:
    - CloudWatch
    - Cost Explorer
    - Trusted Advisor
    - Third party tools can help



# AWS Ecosystem - Free resources

- [AWS Blogs](https://aws.amazon.com/blogs/aws/)
- [AWS Forums (community)](https://forums.aws.amazon.com/index.jspa)
- [AWS Whitepapers & Guides](https://aws.amazon.com/whitepapers)
- [AWS Quick Starts](https://aws.amazon.com/quickstart)
    - Automated, gold-standard deployments in the AWS Cloud
    - Build your production enviromnt quickly with templates
- [AWS Solutions](https://aws.amazon.com/solutions/)
    - Vetted Technology Solutions for the AWS Cloud
    - [Example - AWS Landing Zone: secure, multi-account AWS environment](https://aws.amazon.com/solutions/implementations/aws-landing-zone)
        - "Replaced" by AWS Control Tower



# AWS Ecosystem - AWS Support

### Plans

- Developer
    - Business hours email access to Cloud Support Associates
    - General guidance: < 24 business hours
    - System impaired: < 12 business hours

- Business
    - 24x7 phone, email, and chat access to Cloud Support Engineers
    - Production system impaired: < 4 hours
    - Production system down: < 1 hour

- Enterprise
    - Access to a Technical Account Manager (TAM)
    - Concierge Support Team (for billing and account best practices)
    - Business-critical system down: < 15 minutes



# AWS Ecosystem - AWS Marketplace

Digital catalog with thousands of softwares listing from independent software vendors (Third party)

### Overview

- If you buy through the AWS Marketplace, it goes into you AWS bill
- You can sell  your solutions on the AWS Marketplace

### Example

- Custom AMI (Custom OS, firewalls, technical solutions...)
- CloudFormation templates
- Software as a Service
- Containers



# AWS Ecosystem - AWS Training

- AWS Digital (online) and Classroom Training (in-person or virtual)
- AWS Private Training (for your organization)
- Training and Certification for the U.S. Government
- Training and Certification for the Enterprise
- AWS Academy
    - Helps universities teach AWS
- And your favorite online teacher...
    - Teaching you all about AWS Certifications and more!



# AWS Ecosystem - AWS Professional Services & Partner Network

The AWS Professional Servicesorganization is a global team of experts
They work alongside your team and a chosen member of the APN

- APN = AWS Partner Network
- APN Technology Partners
    - Providing hardware, connectivity, and software
- APN Consulting Partners
    - Pofessional services firm to help build on AWS
- APN Training Partners
    - Find who can help you learn AWS
- AWS Competency Program
    - AWS Competencies are granted to APN Partners who have demonstrated technical proficiency and proven customer success in specialized solution areas
- AWS Navigate Program
    - Help Partners become better Partners



# AWS Knowledge Center

Contains the most frequent & commom questions and requests

- [link](https://aws.amazon.com/premiumsupport/knowledge-center/)
