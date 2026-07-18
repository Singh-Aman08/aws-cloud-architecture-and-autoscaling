# Designing Scalable AWS Architectures for ArtAI (AI Image Processing) and WordFreq (Distributed Data Processing) Applications
## Overview

This project demonstrates the design and optimisation of scalable cloud architectures using **Amazon Web Services (AWS)** for two different application scenarios.

The first application, **ArtAI (AI Image Processing)**, focuses on designing a secure and highly available architecture for an AI-powered image processing platform. The architecture enables users to upload images and receive AI-generated variations while ensuring scalability, low latency, secure model deployment, and reliable data storage.

The second application, **WordFreq (Distributed Data Processing)**, focuses on building a scalable text processing pipeline using AWS services. The system processes uploaded files through an event-driven architecture and uses automatic scaling to dynamically adjust computing resources based on workload demand.

This project explores key cloud computing concepts including **scalability, high availability, fault tolerance, security, monitoring, distributed processing, and cost optimisation**.

## Objectives

The main objectives of this project were:

- Design scalable and secure AWS cloud architectures for AI-powered and distributed data processing applications.

- Develop a highly available architecture for **ArtAI**, ensuring secure AI model deployment, efficient image processing, and reliable data management.

- Build an event-driven processing pipeline for **WordFreq** using cloud-based storage, messaging, compute, and database services.

- Implement workload-based auto-scaling to dynamically adjust computing resources according to application demand.

- Evaluate system performance through load testing and analyse the impact of different scaling strategies and infrastructure configurations.

- Explore architectural improvements to enhance scalability, resilience, security, and cost efficiency using AWS services.
## Methodology

The project followed a structured cloud architecture design and evaluation approach consisting of four main stages:

### 1. Requirement Analysis

The requirements of each application scenario were analysed to identify key cloud design considerations, including scalability, availability, security, performance, and data management.

### 2. AWS Architecture Design

Suitable AWS services were selected based on application requirements, and cloud architectures were designed by defining:

- Application components and service interactions.
- Data flow and communication between AWS services.
- Networking and security considerations.
- Storage, processing, and monitoring strategies.

### 3. Implementation and Scaling

The WordFreq application was deployed using AWS services and enhanced with an automated scaling mechanism. CloudWatch monitoring and Auto Scaling were configured to dynamically manage compute resources according to workload changes.

### 4. Performance Evaluation and Optimisation

The implemented system was evaluated through load testing experiments. Different configurations, including scaling capacity, cooldown periods, monitoring intervals, and instance types, were analysed to understand their impact on performance and identify optimisation opportunities.


## Results and Architecture Outcomes

The project resulted in two scalable AWS-based application architectures designed to address different cloud computing requirements: AI-powered image processing and distributed data processing.

---

## ArtAI Architecture (AI Image Processing)

The final ArtAI architecture provides a secure, highly available, and scalable platform for AI-based image processing.

Key outcomes:

- Designed a globally accessible architecture with low-latency access using AWS content delivery and routing services.
- Deployed the AI inference model securely within a private cloud environment.
- Implemented scalable request handling through load balancing and dynamic resource management.
- Enabled reliable image storage with automated backup and archival strategies.
- Integrated secure access control and monitoring mechanisms to protect application resources.

### ArtAI AWS Architecture

![ArtAI AWS Architecture](images/artai_architecture.png)

---

## WordFreq Architecture (Distributed Data Processing)

The final WordFreq architecture transformed the application into a scalable event-driven processing system.

Key outcomes:

- Implemented an asynchronous processing workflow using cloud storage and message queues.
- Enabled distributed file processing using multiple worker instances.
- Added workload-based auto-scaling to dynamically increase or decrease processing capacity.
- Evaluated different scaling configurations to improve processing efficiency.
- Achieved improved performance through parallel processing and infrastructure optimisation.

### WordFreq AWS Architecture

![WordFreq AWS Architecture](images/wordfreq_architecture.png)

---

## Performance Highlights

Load testing demonstrated that scaling compute resources improved the processing performance of the WordFreq application.

| Optimisation | Impact |
|--------------|--------|
| Increasing worker instances | Improved parallel processing capability |
| Reducing cooldown period | Faster response to workload changes |
| Reducing monitoring interval | Improved scaling responsiveness |
| Increasing EC2 instance capacity | Reduced processing time |

The best observed configuration achieved a processing time of:

**3 minutes 45 seconds**

demonstrating the impact of scalable cloud infrastructure on distributed workloads.
## Conclusion

This project demonstrated the design and optimisation of scalable cloud architectures using AWS for both AI-powered applications and distributed data processing systems.

The ArtAI architecture showed how AWS services can be combined to build a secure, highly available, and scalable AI image processing platform with reliable storage, controlled access, and automated data management.

The WordFreq architecture demonstrated the use of cloud-native services to build an event-driven distributed processing system with workload-based auto-scaling. The performance evaluation highlighted how appropriate scaling strategies and infrastructure choices can improve efficiency and responsiveness.

Overall, this project provided practical experience in cloud architecture design, AWS infrastructure management, distributed systems, auto-scaling, and performance optimisation for scalable applications.
