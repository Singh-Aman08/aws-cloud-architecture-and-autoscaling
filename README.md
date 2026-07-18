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
