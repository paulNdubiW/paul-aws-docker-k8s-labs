# Integrated Docker, Kubernetes, and AWS Curriculum Timetable

**Start Date**: Thursday, July 10, 2025  
**End Date**: Tuesday, September 2, 2025  
**Duration**: 8 weeks (Week 1 partial: July 10-12)  
**Structure**: 
- Self-study on Monday, Tuesday, Thursday, Friday at own pace.
- Lab sessions on Wednesday (covering Monday/Tuesday topics) and Saturday (covering Thursday/Friday topics) via Google Meet.
- Mock interview sessions every two weeks (Wednesdays) via Google Meet, covering topics from the prior two weeks.

## Integrated Curriculum Outline
1. **Module 1: Introduction to Containerization** (Docker)
   - Subtopics:
     - What is containerization: Overview of containers and their role in AWS cloud-native apps (deployed on ECS/EKS).
     - VMs vs Containers: Compare VMs (EC2) with containers (ECS/EKS) for AWS scalability.
     - Benefits: Lightweight, portable containers for AWS ECS/EKS deployments.
     - Docker vs Podman: Docker compatibility with AWS ECS/EKS vs Podman limitations.
   - Lab: Run a Hello World container (push to AWS ECR, deploy on ECS).
2. **Module 2: Docker Installation and Basics**
   - Subtopics:
     - Installing Docker (Windows/macOS/Linux/Cloud): Install Docker on local systems and AWS EC2 instances.
     - CLI essentials (docker run, ps, stop, rm, images): Use Docker CLI to manage containers on EC2 or ECS tasks.
   - Lab: Install Docker on EC2, manage Nginx container (deploy to ECS).
3. **Module 3: Docker Images**
   - Subtopics:
     - Layers, Image IDs: Understand image layers stored in AWS ECR.
     - Pulling/tagging images: Pull from ECR, tag for ECS/EKS deployments.
     - Dockerfile syntax, Multi-stage builds: Write Dockerfiles optimized for AWS ECS/Fargate.
   - Lab: Pull/tag Ubuntu from ECR, build Python Flask app for ECS.
4. **Module 4: Docker Volumes and Data Persistence**
   - Subtopics:
     - Volumes vs Bind Mounts: Use EFS for shared volumes in ECS/Fargate.
     - Managing volumes (create, ls, inspect, rm): Manage EFS volumes for ECS tasks.
   - Lab: Persist MySQL data with EFS volume on ECS.
5. **Module 5: Docker Networking**
   - Subtopics:
     - Network types (Bridge, Host, None, Overlay): Map to AWS VPC networking for ECS.
     - Network management: Configure ECS tasks within VPC subnets.
   - Lab: Connect Nginx + web app via ECS networking in VPC.
6. **Module 6: AWS Cloud Fundamentals**
   - Subtopics:
     - AWS Global Infrastructure: Regions/zones for ECS/EKS deployments.
     - IAM basics: Create roles for ECS/EKS access.
     - Billing and Cost Management: Optimize costs for ECS/EKS clusters.
   - Lab: Set up AWS account, configure IAM roles for ECS/EKS.
7. **Module 7: Kubernetes Architecture**
   - Subtopics:
     - Origins, Comparison with Docker Swarm: Kubernetes on EKS vs Swarm on ECS.
     - Master/Worker nodes (API Server, kubelet, etcd): Deploy EKS control plane and nodes.
     - Kubernetes objects (Pods, Deployments): Manage pods/deployments in EKS.
   - Lab: Set up EKS cluster (alternative: Minikube for local testing).
8. **Module 8: Docker Compose**
   - Subtopics:
     - YAML structure, Multi-container apps: Use Compose for local testing before ECS/EKS deployment.
     - Networking/volumes in Compose: Map to ECS task definitions and EFS.
   - Lab: Build LAMP stack locally, prepare for ECS deployment.
9. **Module 9: Pod Lifecycle and Workloads**
   - Subtopics:
     - Pods, Init Containers, Sidecars: Deploy pods with sidecars in EKS.
     - Labels/Selectors, Deployments/ReplicaSets: Manage EKS deployments.
     - Rolling updates: Perform rolling updates in EKS.
   - Lab: Deploy Nginx app with YAML manifests in EKS.
10. **Module 10: Configuration and Secrets**
    - Subtopics:
      - ConfigMaps: Configure apps in EKS with ConfigMaps.
      - Secrets (encoding vs encryption): Use AWS Secrets Manager with EKS.
      - Mounting configs: Mount Secrets Manager secrets in EKS pods.
    - Lab: Configure app with ConfigMap and Secrets Manager in EKS.
11. **Module 11: Kubernetes Services and Networking**
    - Subtopics:
      - Cluster networking, DNS: Use EKS VPC networking and Route 53.
      - ClusterIP/NodePort/LoadBalancer: Deploy ELB with EKS services.
      - Ingress with NGINX: Configure ALB Ingress Controller in EKS.
    - Lab: Expose 3-tier app via ALB in EKS.
12. **Module 12: AWS Networking and Content Delivery**
    - Subtopics:
      - VPC, Subnets: Configure VPC for ECS/EKS clusters.
      - Route 53, CloudFront, ELB: Use Route 53 and ALB for EKS apps.
    - Lab: Configure VPC, deploy app with ALB in EKS.
13. **Module 13: Volumes and Persistent Storage**
    - Subtopics:
      - Ephemeral vs Persistent storage: Use EBS/EFS for EKS pods.
      - PV/PVC, StorageClasses: Dynamic provisioning with EBS in EKS.
    - Lab: Deploy PostgreSQL with EBS-backed PVC in EKS.
14. **Module 14: AWS Storage and Databases**
    - Subtopics:
      - S3, EBS, EFS: Store data for ECS/EKS apps in S3/EFS.
      - RDS, DynamoDB: Integrate RDS with EKS deployments.
    - Lab: Deploy RDS PostgreSQL, store data in S3 for EKS app.
15. **Module 15: Namespaces and RBAC**
    - Subtopics:
      - Namespaces: Isolate workloads in EKS namespaces.
      - Roles, RoleBindings, ServiceAccounts: Use IAM roles for EKS RBAC.
    - Lab: Create EKS namespace, restrict access with RBAC and IAM.
16. **Module 16: AWS Security, Identity, and Compliance**
    - Subtopics:
      - IAM policies, Security Groups: Secure ECS/EKS with IAM and Security Groups.
      - KMS, Secrets Manager, GuardDuty: Encrypt data, monitor threats in EKS.
    - Lab: Secure EKS app with IAM, KMS, and Security Groups.
17. **Module 17: Observability**
    - Subtopics:
      - Docker logs, Kubernetes logging (EFK): Integrate with CloudWatch in EKS.
      - Prometheus/Grafana, AWS CloudWatch: Monitor EKS with CloudWatch and Prometheus.
    - Lab: Install Prometheus/Grafana in EKS, monitor with CloudWatch.
18. **Module 18: Helm and Package Management**
    - Subtopics:
      - Helm charts, Repositories: Package EKS apps with Helm.
      - Templates, Parameterizing manifests: Deploy Helm charts to EKS.
    - Lab: Package Node.js app with Helm for EKS.
19. **Module 19: Scaling, Affinity, and Scheduling**
    - Subtopics:
      - Manual/Auto scaling: Use HPA in EKS with CloudWatch metrics.
      - Affinity/Anti-affinity, Taints/Tolerations: Schedule pods in EKS.
    - Lab: Simulate autoscaling in EKS with CPU-hungry app.
20. **Module 20: AWS Compute and Serverless**
    - Subtopics:
      - EC2, ECS, EKS: Deploy containers on ECS/EKS.
      - Lambda, Fargate: Run serverless containers with Fargate.
    - Lab: Deploy containerized app to ECS and Lambda function via Fargate.
21. **Module 21: CI/CD and Application Integration**
    - Subtopics:
      - GitHub Actions, Jenkins, ArgoCD: Automate EKS deployments.
      - AWS CodePipeline, CodeBuild, SQS, SNS: Build CI/CD with AWS tools.
    - Lab: Build CodePipeline for EKS app deployment.
22. **Module 22: Final Project - Cloud-Native Microservices Platform**
    - Subtopics:
      - Dockerize services (Product Catalog: Python FastAPI, User Management: Node.js, Orders: Go, Frontend: React): Build images, push to ECR.
      - Kubernetes deployment (EKS, ConfigMaps, Secrets, Ingress, HPA, Helm): Deploy to EKS with ALB and HPA.
      - AWS services (RDS for PostgreSQL, S3 for storage, CloudWatch for monitoring, X-Ray for tracing, CodePipeline for CI/CD): Integrate AWS services for management.
      - NetworkPolicies, Prometheus/Grafana: Secure and monitor EKS cluster.
      - CloudFormation for infrastructure: Define EKS cluster and AWS resources.
    - Lab: Deploy microservices platform on EKS, manage with AWS services (RDS, S3, CloudWatch, CodePipeline).

## Timetable

| Day       | Topic                              | Subtopics                                                                 | Objectives                                                                 | Mode of Study          |
|-----------|------------------------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------|
| **Week 1 (Partial: July 10-12, 2025)** | | | | |
| Thu, Jul 10 | Introduction to Containerization | What is containerization (ECS/EKS), VMs vs Containers (EC2 vs ECS/EKS) | Understand container concepts, AWS deployment options | Self-study |
| Fri, Jul 11 | Introduction to Containerization | Benefits (ECS/EKS), Docker vs Podman (ECS/EKS compatibility) | Compare runtimes, articulate AWS use cases | Self-study |
| Sat, Jul 12 | Lab: Run Hello World Container | Run docker run hello-world, push to ECR, deploy on ECS | Execute and deploy a basic container in AWS | Group (Google Meet) |
| **Week 2 (Jul 14-19)** | | | | |
| Mon, Jul 14 | Docker Installation and Basics | Installing Docker (local/EC2) | Install Docker for AWS environments | Self-study |
| Tue, Jul 15 | Docker Installation and Basics | CLI essentials (manage ECS tasks) | Master Docker CLI for AWS | Self-study |
| Wed, Jul 16 | Lab: Install and Manage Containers | Install Docker on EC2, manage Nginx on ECS | Set up and manage containers in AWS | Group (Google Meet) |
| Thu, Jul 17 | Docker Images | Layers, Image IDs (ECR storage), Pulling/tagging (ECR) | Understand image management in AWS | Self-study |
| Fri, Jul 18 | Docker Images | Dockerfile syntax, Multi-stage builds (ECS/Fargate) | Write Dockerfiles for AWS | Self-study |
| Sat, Jul 19 | Lab: Pull and Build Images | Pull/tag Ubuntu from ECR, build Flask app for ECS | Manage and build images for AWS | Group (Google Meet) |
| **Week 3 (Jul 21-26)** | | | | |
| Mon, Jul 21 | Docker Volumes and Data Persistence | Volumes vs Bind Mounts (EFS for ECS) | Understand AWS storage for containers | Self-study |
| Tue, Jul 22 | Docker Volumes and Data Persistence | Managing volumes (EFS for ECS tasks) | Manage EFS volumes in AWS | Self-study |
| Wed, Jul 23 | Lab: Persist Data with Volumes | Persist MySQL data with EFS on ECS | Implement AWS data persistence | Group (Google Meet) |
| Wed, Jul 23 | Mock Interview | Modules 1-3: Containerization, Installation, Images | Demonstrate Docker fundamentals in AWS | Group (Google Meet) |
| Thu, Jul 24 | Docker Networking | Network types (VPC for ECS) | Understand Docker networking in AWS | Self-study |
| Fri, Jul 25 | Docker Networking | Network management (ECS in VPC subnets) | Configure ECS networking | Self-study |
| Sat, Jul 26 | Lab: Connect Containers | Connect Nginx + web app via ECS in VPC | Set up container communication in AWS | Group (Google Meet) |
| **Week 4 (Jul 28-Aug 2)** | | | | |
| Mon, Jul 28 | AWS Cloud Fundamentals | AWS Global Infrastructure (ECS/EKS regions), IAM basics | Configure AWS for container deployments | Self-study |
| Tue, Jul 29 | AWS Cloud Fundamentals | Billing and Cost Management (ECS/EKS optimization) | Optimize AWS costs | Self-study |
| Wed, Jul 30 | Lab: Set up AWS Account | Set up AWS account, configure IAM for ECS/EKS | Initialize AWS environment | Group (Google Meet) |
| Thu, Jul 31 | Kubernetes Architecture | Origins, Swarm vs EKS, Master/Worker nodes | Understand EKS components | Self-study |
| Fri, Aug 1 | Kubernetes Architecture | Kubernetes objects (Pods/Deployments in EKS) | Manage EKS workloads | Self-study |
| Sat, Aug 2 | Lab: Set up EKS Cluster | Set up EKS cluster (or Minikube locally) | Deploy Kubernetes in AWS | Group (Google Meet) |
| **Week 5 (Aug 4-9)** | | | | |
| Mon, Aug 4 | Docker Compose | YAML structure, Multi-container apps (pre-ECS/EKS) | Design apps for AWS deployment | Self-study |
| Tue, Aug 5 | Docker Compose | Networking/volumes (ECS task definitions, EFS) | Map Compose to AWS ECS | Self-study |
| Wed, Aug 6 | Lab: Build LAMP Stack | Build LAMP stack, prepare for ECS | Deploy multi-container app in AWS | Group (Google Meet) |
| Wed, Aug 6 | Mock Interview | Modules 4-7: Volumes, Networking, AWS Fundamentals, Kubernetes Architecture | Apply Docker/Kubernetes in AWS | Group (Google Meet) |
| Thu, Aug 7 | Pod Lifecycle and Workloads | Pods, Init Containers, Sidecars (EKS), Labels/Selectors | Manage EKS pod lifecycles | Self-study |
| Fri, Aug 8 | Pod Lifecycle and Workloads | Deployments/ReplicaSets, Rolling updates (EKS) | Perform EKS updates | Self-study |
| Sat, Aug 9 | Lab: Deploy Nginx App | Deploy Nginx with YAML in EKS | Deploy Kubernetes workloads in AWS | Group (Google Meet) |
| **Week 6 (Aug 11-16)** | | | | |
| Mon, Aug 11 | Configuration and Secrets | ConfigMaps (EKS), Secrets (Secrets Manager) | Configure EKS apps | Self-study |
| Tue, Aug 12 | Configuration and Secrets | Mounting configs (Secrets Manager in EKS) | Manage sensitive data in EKS | Self-study |
| Wed, Aug 13 | Lab: Configure App | Configure app with ConfigMap/Secrets Manager in EKS | Implement EKS configuration | Group (Google Meet) |
| Thu, Aug 14 | Kubernetes Services and Networking | Cluster networking, DNS (EKS VPC, Route 53) | Understand EKS networking | Self-study |
| Fri, Aug 15 | Kubernetes Services and Networking | ClusterIP/NodePort/LoadBalancer, Ingress (ALB in EKS) | Configure EKS external access | Self-study |
| Sat, Aug 16 | Lab: Expose 3-Tier App | Expose 3-tier app via ALB in EKS | Set up EKS service routing | Group (Google Meet) |
| **Week 7 (Aug 18-23)** | | | | |
| Mon, Aug 18 | AWS Networking and Content Delivery | VPC, Subnets (ECS/EKS), Route 53 | Configure AWS networking for containers | Self-study |
| Tue, Aug 19 | AWS Networking and Content Delivery | CloudFront, ELB (ALB for EKS) | Deploy apps with AWS content delivery | Self-study |
| Wed, Aug 20 | Lab: Configure VPC and ALB | Configure VPC, deploy app with ALB in EKS | Set up AWS networking | Group (Google Meet) |
| Wed, Aug 20 | Mock Interview | Modules 8-11: Compose, Pods, Configuration, Kubernetes Networking | Demonstrate AWS-integrated Kubernetes skills | Group (Google Meet) |
| Thu, Aug 21 | Volumes and Persistent Storage | Ephemeral vs Persistent storage, PV/PVC (EBS/EFS in EKS) | Manage EKS storage | Self-study |
| Fri, Aug 22 | Volumes and Persistent Storage | StorageClasses (EBS in EKS) | Implement dynamic provisioning in EKS | Self-study |
| Sat, Aug 23 | Lab: Deploy PostgreSQL | Deploy PostgreSQL with EBS-backed PVC in EKS | Manage EKS persistent storage | Group (Google Meet) |
| **Week 8 (Aug 25-Sep 2)** | | | | |
| Mon, Aug 25 | AWS Storage and Databases | S3, EBS, EFS (ECS/EKS storage) | Manage AWS storage for containers | Self-study |
| Tue, Aug 26 | AWS Storage and Databases | RDS, DynamoDB (integrate with EKS) | Deploy AWS databases for EKS | Self-study |
| Wed, Aug 27 | Lab: Deploy RDS and S3 | Deploy RDS PostgreSQL, store data in S3 for EKS | Integrate AWS storage/databases | Group (Google Meet) |
| Thu, Aug 28 | Final Project | Dockerize services (FastAPI, Node.js, Go, React), push to ECR, deploy to EKS | Containerize and deploy microservices in AWS | Self-study |
| Fri, Aug 29 | Final Project | EKS deployment (ConfigMaps, Secrets, ALB, HPA, Helm), RDS, S3, CloudWatch | Integrate AWS services with EKS | Self-study |
| Sat, Aug 30 | Lab: Microservices Platform Part 1 | Deploy services with Helm on EKS, integrate RDS/S3 | Implement AWS microservices deployment | Group (Google Meet) |
| Mon, Sep 1 | Final Project | NetworkPolicies, Prometheus/Grafana, CodePipeline, X-Ray, CloudFormation | Secure, monitor, automate AWS deployment | Self-study |
| Tue, Sep 2 | Final Project | Review and optimize platform, test with CloudWatch/X-Ray | Finalize AWS microservices system | Self-study |
| Tue, Sep 2 | Mock Interview | Modules 12-22: AWS Networking, Storage, Security, Observability, Helm, Scaling, Compute, CI/CD, Final Project | Demonstrate comprehensive AWS cloud-native skills | Group (Google Meet) |

## Mock Interview Topics
- **Week 3 (Jul 23)**: Modules 1-3 (Containerization, Installation, Images)
- **Week 5 (Aug 6)**: Modules 4-7 (Volumes, Networking, AWS Fundamentals, Kubernetes Architecture)
- **Week 7 (Aug 20)**: Modules 8-11 (Compose, Pods, Configuration, Kubernetes Networking)
- **Week 8 (Sep 2)**: Modules 12-22 (AWS Networking, Storage, Security, Observability, Helm, Scaling, Compute, CI/CD, Final Project)
