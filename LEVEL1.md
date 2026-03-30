## CL - Cloud Computing

### **Task 1: Working with Git and GitHub Basics**

**Task Description**  
Start by understanding version control. Practice cloning repositories, making changes, committing those changes, and pushing them back to GitHub. Create branches and open pull requests to simulate collaborative workflows. Learn to review and merge pull requests to complete the development cycle. 
  
**Expected Task Outcomes**  
•	Understand the fundamentals of version control and distributed repositories   
•	Learn how to solve merge conflict - git rebase   
•	Create and manage branches for feature development    
•	Contribute to atleast one open source project   
• Implement and learn about git revert, git cherry-pick  
• Create a customized Git workflow - Git config   
    
**Resource Links**  
•	Git Official Documentation: https://git-scm.com/doc     
•	GitHub Learning Lab: https://github.com/apps/github-learning-lab   
•	Pro Git Book (free): https://git-scm.com/book/en/v2    


### **Task 2: Exploring Docker Fundamentals**
**Task Description**  
Begin with learning the difference between containers and virtual machines. Practice using Docker CLI commands to pull images from Docker Hub, run containers, inspect running processes, view logs, and manage container lifecycles such as stopping and removing containers.  
  
**Expected Task Outcomes**  
•	Articulate the key differences between containers and virtual machines  
•	Pull images from Docker Hub and run containers using CLI commands   
•	Inspect running processes, view container logs, and understand container state  
•	Manage full container lifecycles: start, stop, restart, and remove   
  
**Resource Links**  
•	Docker Official Documentation: https://docs.docker.com/  
•	Docker Hub: https://hub.docker.com/   
•	Play with Docker (browser-based lab): https://labs.play-with-docker.com/   

### **Task 3: Dockerize a Simple Application**  

**Task Description**   
Learn Dockerfile basics and how to containerize applications. Write a Dockerfile for a simple static website or API provided as starter code. Build your Docker image from this Dockerfile and run the application container locally. Verify successful deployment by accessing the app from your browser.  
  
**Expected Task Outcomes**   
•	Write a functional Dockerfile to containerize a provided application  
•	Build a Docker image and run it as a container on your local machine  
•	Map container ports to the host machine to access the app in a browser   
•	Understand image layers and how each Dockerfile instruction creates a layer   
  
**Resource Links**   
•	Dockerfile Reference: https://docs.docker.com/engine/reference/builder/   
•	Best Practices for Writing Dockerfiles: https://docs.docker.com/develop/develop-images/dockerfile_best-practices/  


### **Task 4: Launch and Manage an AWS EC2 Instance**  

**Task Description**  
Explore AWS EC2 service and different instance types. Launch a free-tier EC2 instance, configure the security group to allow SSH access, and connect securely using SSH. Install a lightweight web server such as Nginx or Apache on the instance and ensure it is accessible via the public IP. Also, understand how CPU and memory work in a VM.  
  
**Expected Task Outcomes**   
•	Launch an EC2 instance using the AWS Free Tier and configure its security group  
•	Connect to the instance securely over SSH using a .pem key pair  
•	Install and start a web server (Nginx or Apache) and confirm access via public IP  
•	Understand EC2 instance types, CPU credits, and memory allocation in cloud VMs  
  
**Resource Links**   
•	AWS EC2 Getting Started Guide: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html  
•	AWS Free Tier Details: https://aws.amazon.com/free/  
•	Nginx Beginner's Guide: https://nginx.org/en/docs/beginners_guide.html  
  
### **Task 5: Kubernetes Basics and Writing Pod Specs**

**Task Description**  
Understand key Kubernetes concepts and the structure of YAML manifest files. Write a simple Pod specification YAML to run a basic container (e.g., Nginx). Apply the manifest to your Minikube cluster and verify the Pod is running. Explore commands to get Pod status and logs.  
  
**Expected Task Outcomes**  
•	Explain core Kubernetes concepts: Nodes, Pods, Clusters, and the Control Plane  
•	Write a valid Pod manifest YAML file to deploy a container image  
•	Apply manifests to a local Minikube cluster using kubectl  
•	Use kubectl commands to inspect Pod status, describe Pods, and view logs    
  
**Resource Links**  
•	Kubernetes Official Documentation: https://kubernetes.io/docs/home/  
•	Minikube Getting Started: https://minikube.sigs.k8s.io/docs/start/  
•	Kubernetes YAML Basics: https://kubernetes.io/docs/concepts/workloads/pods/  


### **Task 6: Manage AWS S3 and IAM with CLI**  

**Task Description**  
Study AWS IAM concepts like users, roles, and policies, and learn to configure the AWS CLI. Create an IAM user with permissions to access S3, then create an S3 bucket from the CLI. Practice uploading, listing, and downloading files to/from the bucket using AWS CLI commands, reinforcing cloud storage handling.  
   
**Expected Task Outcomes**  
•	Understand IAM concepts: users, groups, roles, and least-privilege policies  
•	Configure the AWS CLI with credentials and verify connectivity to AWS services  
•	Create an S3 bucket and manage objects via CLI (upload, list, download, delete)  
•	Apply IAM policies to restrict S3 access to specific users or roles  
   
**Resource Links**  
•	AWS IAM Documentation: https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html  
•	AWS CLI S3 Command Reference: https://docs.aws.amazon.com/cli/latest/reference/s3/  
•	AWS S3 Getting Started: https://docs.aws.amazon.com/AmazonS3/latest/userguide/GetStartedWithS3.html  
  
  
### **Task 7: Deploy a Containerized Application on Kubernetes**  
**Task Description**  
Learn to write YAML manifests for Kubernetes deployments and services. Package your Dockerized app and deploy it using YAML files. Expose the app within the cluster via ClusterIP and externally using NodePort.   Validate by accessing the app through the configured NodePort on your local machine.  
  
**Expected Task Outcomes**  
•	Write Deployment YAML to deploy multiple replicas of a containerized application  
•	Expose the deployment within the cluster using a ClusterIP Service  
•	Expose the deployment externally using a NodePort Service and access it in a browser  
•	Scale deployments up and down using kubectl and observe rolling updates  
  
**Resource Links**  
•	Kubernetes Deployments: https://kubernetes.io/docs/concepts/workloads/controllers/deployment/  
•	Kubernetes Services: https://kubernetes.io/docs/concepts/services-networking/service/  
  
  
### **Task 8: Use Kubernetes Secrets and Environment Variables**  
  
**Task Description**  
Understand how to handle sensitive data and configuration within Kubernetes using Secrets and ConfigMaps. Create a ConfigMap and mount it onto a deployment and let the underlying application use the configuration. Create a Kubernetes Secret with AWS credentials, update deployment YAML to use these Secrets as environment variables, and deploy the updated app. Verify that the app uses the credentials securely to interact with AWS S3.  
   
**Expected Task Outcomes**  
•	Create and apply ConfigMaps to inject non-sensitive configuration into Pods  
•	Create Kubernetes Secrets to store AWS credentials without hardcoding them  
•	Mount Secrets as environment variables in a Deployment and verify their consumption  
•	Understand the difference between Secrets and ConfigMaps and when to use each 
  
**Resource Links**  
•	Kubernetes Secrets: https://kubernetes.io/docs/concepts/configuration/secret/  
•	Kubernetes ConfigMaps: https://kubernetes.io/docs/concepts/configuration/configmap/  
  
### **Task 9: Deploy an App to Push Files from Kubernetes to S3**  
  
**Task Description**  
Build and deploy an application on Kubernetes capable of pushing files from a locally hosted app server to AWS S3. Use Kubernetes Secrets for storing AWS credentials securely. Validate the file upload process from the app interface to the S3 bucket and verify files in the cloud storage.   
  
**Expected Task Outcomes**  
•	Build and containerize a file-upload application using a language/framework of your choice  
•	Deploy the app on Minikube with AWS credentials injected via Kubernetes Secrets  
•	Successfully upload a file from the app UI/CLI and verify it appears in the S3 bucket  
•	Integrate all Level 1 concepts: Docker, Kubernetes, IAM, S3, and Secrets into one working pipeline  
  
**Resource Links**  
•	AWS SDK for Python (boto3): https://boto3.amazonaws.com/v1/documentation/api/latest/index.html  
•	AWS SDK for Node.js: https://docs.aws.amazon.com/AWSJavaScriptSDK/v3/latest/  
•	Kubernetes Secrets in Pods: https://kubernetes.io/docs/tasks/inject-data-application/distribute-credentials-secure/  
  
---  
  
## CY - Cybersecurity  
Welcome to the Marvel Cybersecurity Module.    
Level 1 of this module is designed to build a strong foundation by covering the essentials of computer networking, protocols, Windows, Linux, and core cybersecurity principles. These fundamentals are crucial—  cybersecurity is not just about tools, but about understanding how systems work.  
At its core, cybersecurity follows simple logic:  
 _You can’t protect what you can’t see (or don’t understand), and you can’t break what you don’t know.  
 That’s why mastering these basics is the first step toward becoming skilled in both defending and attacking systems._  
Once you complete Level 1, we’ll move into the more exciting part—hands-on hacking and defense techniques. Stay tuned!  
   
Getting Started  
To begin, you’ll need access to a platform called TryHackMe, where all course materials are hosted. Please follow the steps below to create your account:   
Step 1: Go to https://tryhackme.com/  
Step 2: Click on “Join for FREE” (top-right corner)  
<img width="1167" height="666" alt="image" src="https://github.com/user-attachments/assets/36527282-5926-4c61-b93f-0310bfa81ef9" />  
Step 3: Sign up using your Google, LinkedIn, or email account  
Step 4: Complete any required details (password, captcha, etc.)  
Step 5: Finish the introductory tour on the platform  
Step 6: Access the Level 1 module using the link below: https://tryhackme.com/jr/uvce_marvel_level1  
