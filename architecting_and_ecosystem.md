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

## Performance Efficiency

## Cost Optmization