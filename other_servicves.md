# Amazon Workspaces

Managed Desktop as a Service (Windows or Linux)

## Overview

- Fully managed Virtual Desktop Infraestucture (VDI)
- The users connect to the VDI and open native applications
- Workspaces are on-demand or always on

## Price

- Pay-as-you-go service with monthly or hourly rates

## Best Practice

- Deploy the service as close as possible to the users, to minimize the latency



# Amazon AppStream 2.0

Desktop Application Streaming Service

## Overview

- Deliver to any computer, without acquiring, provisioning infraestructure
- The application is delivered from within a web browser
- Works with any device
- Allow to configure an instance type per application type (CPU, RAMM and GPU)



# Amazon Sumerian

Create and run virtual reality (VR), augmented reality (AR) and 3 applications

## Overview

- Can be used to quickly create 3D models with animations
- Ready-to-use templates and assets, no programming or 3D expertise required
- Acessible via a web-browser URLs or on popular hardware for AR/VR

## Example

- [link](https://docs.aws.amazon.com/sumerian/latest/userguide/gettingstarted-showcase.html)



# AWS Iot Core

Allows you to easily connect IoT devices to the AWS Cloud

## Overview

- Serverless, secure & scalable to billions of devices and trilions of messages
- Your applications can communicate with your devices even when they aren't connected
- Integrates with a lot of AWS services (Lambda, S3, SageMaker, etc.)
- Build IoT applications that gather, process, analyze and act on data



# Amazon Elastic Transcoder

Is used to convert media files tored in S3 into media files in the formats required by consumer playback devices (phones, tablets, pc, etc)

## Overview

- Easy to use
- Higly scalable, can handle large volumes of media files and large files sizes

## Price

- Duration-based pricing model



# AWS Device Farm

Fully-managed service that tests your web and mobile apps against desktop browsers, real mobile devices and tablets

## Overview

- Run tests concurrently on multiple devices (speed up execution)
- Ability to configure devices settings (GPS, lnguage, Wi-Fi, Bluetooth, etc)



# AWS Backup

Fully-managed service to centrally manage and automate backups across AWS services

## Overview

- On-demand and scheduled backups
- Supports Point-in-time Recovery (PITR)
- Retention periods, Lifecycle Management, Backup Policies, etc
- Cross-Region Backup
- Cross-Account Backup (using AWS Organizations)

## How it works

- Create a backup plan
- Assign AWS Resource like EC2, EBS, RDS, DynamoDB, etc
- Automatically backed up to Amazon S3



# Disaster Recovery Strategies

When the company has on-demand machines and a disaster occurs, the aws will be used do recovery data or application

## Plans

- Backup and Restore
    - Restore data from S3 backup

- Pilot Light
    - Restore core functions of the app
    - Ready to scale, but minimal setup

- Warm Standby
    - Full version of the app
    - Minimun size

- Multi-Site / Hot-Site
    - Full version of the app
    - Full size



# CloudEndurance Disaster Recovery

Quickly and easily recover your phisical, virtual and cloud-based servers int AWS

## Overview

- Continuous block-level replication for your own servers

## Example

- Protect your most critical databases (including Oracle, MySQL and SQL Server), enterprise app (SAP), protect yopur data from ransomware attacks, etc



# AWS DataSync

Move large amount of datafrom on-premises to AWS

## Overview

- Can synchronize to: Amazon S3 (any storage classes - including Glacier), Amazo EFS and Amazon FSx for Windows
- Replication tasks can be scheduled hourly, daily and weekly
- The replication tasks are __incremental__ after first full load

## Example

- A datasync software will be installed into the on-premises server
- The software will be connected to the AWS DataSync and send the data directly into S3, EFS or FSx



# AWS Fault Injection Simulator (FIS)

A Fully managed service for running fault injection experiments on AWS workloads

## Overview

- Based on __Chaos Engineering__, stressing an application by creating disruptive events (e.g., sudden increase in CPU or Memory), observing how the system responds and  implementing improvements
- Helps you uncover hidden bugs and performance bottlenecks
- Supports the following AWS services: EC2, ECS, EKS, RDS, etc
- Use pre-built templates that generate the desired disruptions

## Example

- Create a experiment template
- Start the experiment
- Attack resources and get values from it using monitoring softwares like Cloudwatch
- Stop the experiment
- View results
- Do refactor or upgrades
