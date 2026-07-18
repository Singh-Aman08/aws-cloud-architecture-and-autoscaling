# Designing Scalable AWS Architectures for ArtAI (AI Image Processing) and WordFreq (Distributed Data Processing) Applications
## Overview
This project demonstrates the design and optimisation of scalable cloud architectures using Amazon Web Services (AWS) for two different application scenarios.

The first architecture focuses on **ArtAI**, an AI-powered image processing application where users upload images and receive AI-generated variations. The architecture is designed to provide high availability, low latency, secure AI model deployment, and automated data backup using AWS services.

The second architecture focuses on **WordFreq**, a distributed text processing application that analyses uploaded files and generates word frequency results. The application was deployed using AWS storage, messaging, compute, and database services, with an Auto Scaling mechanism implemented to dynamically adjust processing capacity based on workload.

The project explores AWS cloud design principles including scalability, fault tolerance, security, monitoring, cost optimisation, and distributed processing.
## Objectives

The main objectives of this project were:

- **Design scalable AWS architectures:** Develop cloud-based architectures for different application scenarios by selecting appropriate AWS services for compute, storage, networking, security, and monitoring requirements.

- **Build a secure AI application architecture:** Design the ArtAI platform with secure AI model deployment, ensuring that the inference model is accessible only through the application backend while providing reliable image processing capabilities.

- **Develop highly available cloud solutions:** Apply AWS availability and reliability principles using services such as Availability Zones, Elastic Load Balancing, Auto Scaling, and managed AWS storage solutions.

- **Implement distributed data processing workflows:** Deploy the WordFreq application using AWS services such as Amazon S3, SQS, EC2, and DynamoDB to create a scalable event-driven processing pipeline.

- **Implement workload-based auto-scaling:** Configure AWS Auto Scaling and CloudWatch monitoring to dynamically increase or decrease compute resources based on the number of pending processing jobs.

- **Evaluate system performance:** Perform load testing experiments to analyse the impact of scaling capacity, instance types, cooldown periods, and monitoring intervals on application performance.

- **Optimise cloud architecture:** Explore improvements using serverless and distributed processing solutions to enhance resilience, cost efficiency, and scalability.

- **Apply cloud security best practices:** Utilise AWS IAM, VPC networking, authentication mechanisms, and encryption strategies to protect application resources and data.

## Methodology

The project methodology involved designing, implementing, and evaluating two AWS-based application architectures. Each architecture followed a structured approach of requirement analysis, AWS service selection, system design, deployment/scaling strategy, and performance evaluation.

---

## 1. ArtAI Architecture Methodology (AI-Powered Image Processing)

The ArtAI architecture was designed by first identifying the requirements of a global AI image processing service, including low-latency access, secure AI model deployment, high availability, and automated data management.

The methodology involved:

- **Requirement analysis:** Identifying key application requirements such as worldwide accessibility, secure model hosting, scalable inference capability, and reliable image storage.

- **AWS service selection:** Selecting suitable AWS services based on their role in the application:
  - Amazon CloudFront and Route 53 for global access and traffic routing.
  - Elastic Load Balancer and Auto Scaling for handling variable user demand.
  - Amazon EC2 for hosting the AI inference model.
  - Amazon S3 for storing uploaded and generated images.
  - DynamoDB for storing image metadata.
  - Cognito and IAM for authentication and access control.

- **Secure architecture design:** The AI model was placed inside private EC2 instances within a VPC to prevent direct public access. Security groups, IAM roles, and controlled service communication were considered to protect application resources.

- **Data backup strategy:** S3 lifecycle policies were designed to automatically move older images to S3 Glacier for long-term archival and recovery.

- **Monitoring and reliability:** CloudWatch monitoring and alarms were incorporated to track application usage and trigger notifications during high request volumes.

---

## 2. WordFreq Architecture Methodology (Distributed Text Processing)

The WordFreq architecture methodology focused on transforming a single-worker processing system into a scalable distributed processing pipeline.

The methodology involved:

- **Initial architecture deployment:** Setting up the core AWS infrastructure:
  - Amazon S3 for file storage.
  - Amazon SQS for asynchronous job handling.
  - Amazon EC2 for running worker instances.
  - Amazon DynamoDB for storing processing results.

- **Event-driven workflow design:** Implementing an event-based pipeline where file uploads to S3 generate messages in SQS, allowing EC2 workers to process files independently.

- **Auto-scaling implementation:** Designing workload-based scaling using the SQS queue length metric:
  - CloudWatch monitored the number of pending processing jobs.
  - Auto Scaling Groups dynamically launched or terminated EC2 worker instances based on workload.

- **Performance evaluation:** The system was tested with multiple text files to analyse:
  - Scaling capacity impact.
  - Cooldown period optimisation.
  - CloudWatch evaluation frequency.
  - EC2 instance type performance.

- **Architecture optimisation:** Alternative approaches such as AWS Lambda and Amazon EMR-based processing frameworks were analysed to improve cost efficiency, scalability, and fault tolerance.

## Results and Architecture Outcomes

The project resulted in two scalable AWS-based application architectures designed to address different cloud computing requirements: AI-powered image processing and distributed data processing.

---

## 1. ArtAI Architecture Result

The final ArtAI architecture provides a secure, highly available, and scalable platform for AI-based image processing.

Key outcomes:

- Designed a globally accessible application using Amazon Route 53 and CloudFront for low-latency user access.
- Implemented secure AI model deployment using EC2 instances inside a private VPC.
- Enabled scalable inference processing using Elastic Load Balancing and Auto Scaling.
- Used Amazon S3 for durable image storage with lifecycle-based backup to S3 Glacier.
- Integrated DynamoDB for efficient metadata management.
- Applied IAM roles, Cognito authentication, and network security controls to protect application resources.

### ArtAI AWS Architecture

![ArtAI AWS Architecture](images/artai_architecture.png)

---

## 2. WordFreq Architecture Result

The final WordFreq architecture transformed a single-worker application into a scalable distributed processing system using AWS services.

Key outcomes:

- Developed an event-driven processing workflow using Amazon S3 and SQS.
- Enabled asynchronous job processing through message queues.
- Implemented EC2-based worker scaling using CloudWatch metrics and Auto Scaling Groups.
- Achieved improved processing performance through parallel execution.
- Evaluated different scaling configurations to optimise workload handling.

### WordFreq AWS Architecture

![WordFreq AWS Architecture](images/wordfreq_architecture.png)

---

## Performance Highlights

Load testing demonstrated that increasing processing capacity significantly improved performance.

| Experiment | Result |
|------------|--------|
| Increased worker instances | Reduced overall processing time through parallel processing |
| Reduced cooldown period | Faster response to workload changes |
| Reduced monitoring interval | Improved scaling responsiveness |
| Larger EC2 instances | Improved computation performance |

The best observed configuration achieved a processing time of **3 minutes 45 seconds** using a larger EC2 instance type, demonstrating the impact of resource scaling on distributed workloads.

## Conclusion

This project demonstrated the design and optimisation of scalable cloud architectures using AWS for both AI-powered applications and distributed data processing systems.

The ArtAI architecture showed how AWS services can be combined to build a secure, highly available, and scalable AI image processing platform with reliable storage, authentication, monitoring, and automated backup mechanisms.

The WordFreq architecture demonstrated the implementation of an event-driven distributed processing pipeline using AWS services such as S3, SQS, EC2, DynamoDB, CloudWatch, and Auto Scaling. The scaling experiments highlighted how workload-based resource management can improve application performance and cost efficiency.

Overall, the project provided practical experience in cloud architecture design, AWS infrastructure management, distributed computing, auto-scaling strategies, and performance optimisation for scalable applications.

