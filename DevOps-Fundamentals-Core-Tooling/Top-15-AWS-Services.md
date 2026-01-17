- AWS offers 200+ services

<img width="1697" height="864" alt="image" src="https://github.com/user-attachments/assets/6ca6781b-3c18-4edc-9bfb-619bd75796cb" />
<img width="1392" height="822" alt="image" src="https://github.com/user-attachments/assets/93d2baa0-cb75-4179-b2ce-6577f3cddaa3" />
<img width="1326" height="624" alt="image" src="https://github.com/user-attachments/assets/1beac516-3409-466d-aee4-0a2ad4acdb43" />

**EC2 (Elastic Compute Cloud)**: A fundamental service for deploying web applications and dynamic applications, allowing exposure to the external world (4:53).

**VPC (Virtual Private Cloud):** Crucial for securing AWS resources, especially EC2 instances, by managing security groups, CIDR blocks, and traffic rules (5:11).

**EBS (Elastic Block Store) / Volumes:** Important for understanding how to attach additional storage to EC2 instances for applications that generate or store large amounts of data, facilitating backups and snapshots (6:51).

**S3 (Simple Storage Service) Buckets:** A widely used, cost-effective, and scalable storage service for various data types, now encrypted by default for enhanced security (8:03).

**IAM (Identity and Access Management):** A critical service for managing user permissions and access to AWS resources, ensuring proper security and preventing misuse (10:30).

**CloudWatch:** An essential monitoring and observability service that tracks all actions within AWS, allowing for alerts and automated responses to events (12:56).

**Lambda:** A serverless compute service used for executing short, event-driven actions, often in conjunction with CloudWatch, for tasks like encrypting unencrypted volumes (15:38). remember about if in case user created unencrypted volume then automatically it will get deleted and lambda will create encrypted volume

**AWS Cloud Build Services (Code Pipeline, Code Build, Code Deploy):** These services enable Continuous Integration (CI) and Continuous Delivery (CD) on AWS.

   - Code Pipeline: Similar to Jenkins pipelines, it orchestrates the CI/CD workflow (21:18).
   - Code Build: A fully managed build service that compiles code, runs tests, and packages software (21:41).
   - Code Deploy: Manages the deployment of applications onto EC2 instances or on-premises servers (21:56).


**AWS Configuration:** A guardrail service that helps monitor and ensure compliance with organizational configuration standards, such as requiring encrypted EBS volumes (24:40).

**Billing and Costing:** Understanding this service is crucial for monitoring organizational spending on AWS resources like EC2, S3, and EBS (25:31).

**AWS KMS (Key Management Service):** Used for managing encryption keys, secrets, and certificates to secure sensitive data and configurations (26:30).

**CloudTrail:** Records API activities and preserves logs for auditing and risk assessment, providing a historical record of events on AWS (28:13).

**AWS EKS (Elastic Kubernetes Service):** A managed Kubernetes service, essential for DevOps engineers dealing with containerized applications (30:05).

**AWS Fargate and ECS (Elastic Container Service):** Other container services offered by AWS. ECS is AWS's proprietary container orchestration solution, while Fargate allows running containers without managing servers (31:11).
ELK Stack (Elasticsearch, Logstash, Kibana): Important for efficient logging and monitoring of microservices, allowing for analysis of application errors and performance (32:22).
