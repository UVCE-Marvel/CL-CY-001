## CL - Cloud Computing

### **Task 1: Linux Fundamentals and Shell Scripting**

**Task Description**  
Build a practical understanding of Linux fundamentals, including file permissions, process management, disk usage, and environment variables. Write Bash scripts to inspect system usage and running processes, then schedule a script with `cron` and verify that its output is logged correctly.

**Expected Task Outcomes**  
• Understand Linux file permissions, process management, and environment variables  
• Write a Bash script that checks disk usage for each directory under `/home` and prints a warning if any directory exceeds 80% usage  
• Write a Bash script that accepts a process name, checks whether it is running, and reports its PID and memory usage  
• Display a friendly error message when the requested process is not running  
• Schedule the process-checking script to run every five minutes using `cron`  
• Configure and verify logging so that scheduled script output is recorded correctly  

**Resource Links**  
• GNU Bash Reference Manual: https://www.gnu.org/software/bash/manual/  
• Linux man-pages project: https://man7.org/linux/man-pages/  
• `cron` and crontab reference: https://man7.org/linux/man-pages/man5/crontab.5.html  
• ShellCheck (Bash script analysis): https://www.shellcheck.net/  


### **Task 2: Networking Fundamentals and SSH**

**Task Description**  
Understand how data travels across networks and how to inspect network connectivity, DNS resolution, HTTP traffic, and open ports. Use command-line networking tools to investigate two websites, interpret their output in plain English, examine services running on an EC2 instance, and configure SSH key-based authentication between two EC2 instances.

**Expected Task Outcomes**  
• Run `traceroute` against two websites and explain what each hop represents  
• Identify which traceroute hops appear to belong to AWS and which are outside AWS, documenting any uncertainty where ownership cannot be established  
• Use `nslookup` and `dig` to resolve a domain and explain the important lines in their output  
• Run `netstat -tulnp` on an EC2 instance, identify the service associated with each listening port, and assess whether that port should be publicly accessible  
• Use `curl -v` to make an HTTP request and annotate the request headers, response headers, status code, and response body  
• Generate an SSH key pair using `ssh-keygen`, copy the public key to a second EC2 instance using `ssh-copy-id`, and verify passwordless login  

**Resource Links**  
• Linux `traceroute` manual: https://man7.org/linux/man-pages/man8/traceroute.8.html  
• `dig` manual: https://bind9.readthedocs.io/en/latest/manpages.html  
• `nslookup` documentation: https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/nslookup  
• curl command-line tool documentation: https://curl.se/docs/  
• OpenSSH manual pages: https://www.openssh.com/manual.html  
• Amazon EC2 security groups: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html  


### **Task 3: Deploy a Public-Facing App on AWS EC2**

**Task Description**  
Take a Dockerized application from Level 1 and deploy it on an AWS EC2 instance so that it can be accessed over the internet using a public IP address. Install Docker on a fresh instance, run the application container on port 80, configure inbound HTTP access, and practise manually updating the deployed application after publishing a new image to Docker Hub.

**Expected Task Outcomes**  
• Connect to a fresh EC2 instance over SSH and install Docker  
• Pull the application's Docker image from Docker Hub  
• Run the container with the application available on port 80  
• Configure the EC2 security group to allow inbound HTTP traffic on port 80  
• Access the application through a browser using the EC2 public IP address and verify that it is live  
• Make a small change to the application locally, build and push an updated image to Docker Hub, then pull and redeploy the image on EC2 manually  

**Resource Links**  
• Amazon EC2 Getting Started Guide: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html  
• Docker Engine installation: https://docs.docker.com/engine/install/  
• Docker image build documentation: https://docs.docker.com/build/  
• Docker Hub documentation: https://docs.docker.com/docker-hub/  
• EC2 security groups: https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html  


### **Task 4: Introduction to Databases**

**Task Description**  
Learn what a relational database is and why applications use persistent storage instead of keeping all data in memory. Practise basic SQL operations, run a MySQL container as a Kubernetes Pod, connect to it with `kubectl exec`, and observe what happens to data when the Pod is restarted without persistent storage.

**Expected Task Outcomes**  
• Explain relational databases and the meaning of tables, rows, and columns  
• Describe why applications cannot rely on in-memory storage for data that must survive process or system restarts  
• Create a database table and practise SQL `INSERT`, `SELECT`, `UPDATE`, and `DELETE` operations  
• Write a Kubernetes Pod manifest that runs a MySQL container and passes database credentials through environment variables  
• Connect to the running Pod using `kubectl exec` and execute SQL queries inside the container  
• Restart the Pod and observe that data stored only in the container's ephemeral filesystem is lost; explain the role of persistent storage  

**Resource Links**  
• MySQL Reference Manual: https://dev.mysql.com/doc/refman/8.4/en/  
• SQL statements in MySQL: https://dev.mysql.com/doc/refman/8.4/en/sql-statements.html  
• Kubernetes Pods: https://kubernetes.io/docs/concepts/workloads/pods/  
• Run a command in a container: https://kubernetes.io/docs/tasks/debug/debug-application/get-shell-running-container/  
• Kubernetes volumes: https://kubernetes.io/docs/concepts/storage/volumes/  


### **Task 5: CI/CD Pipeline with GitHub Actions**

**Task Description**  
Automate the manual application redeployment process from Task 3 by creating a CI/CD workflow with GitHub Actions. Start from the provided YAML template, understand its triggers, jobs, steps, and secrets, then configure it to build and publish a Docker image whenever changes are pushed to `main`. Add an SSH-based deployment step that updates the application running on EC2.

**Expected Task Outcomes**  
• Explain what Continuous Integration (CI) and Continuous Delivery/Deployment (CD) mean and why they are useful  
• Set up a GitHub Actions workflow using the provided YAML template  
• Understand the workflow's triggers, jobs, steps, and secrets  
• Configure the workflow to build a Docker image and push it to Docker Hub on every push to `main`  
• Store required credentials and connection details in GitHub Actions secrets rather than hardcoding them in the workflow  
• Add a deployment step that connects to EC2 over SSH, pulls the updated image, and restarts the container  
• Push a code change, observe the workflow run end to end, and verify that the update is live without manually operating the server  

**Resource Links**  
• GitHub Actions documentation: https://docs.github.com/en/actions  
• Understanding GitHub Actions: https://docs.github.com/en/actions/about-github-actions/understanding-github-actions  
• Using secrets in GitHub Actions: https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions  
• Docker build and push action: https://github.com/docker/build-push-action  
• Docker Hub documentation: https://docs.docker.com/docker-hub/  


### **Task 6: Kubernetes Services**

**Task Description**  
Understand how Kubernetes Services provide network access to applications running inside a cluster. Deploy an application on Minikube and expose it using `ClusterIP`, `NodePort`, and `LoadBalancer`. Test how each service type can be reached and compare the use cases and networking behaviour of the three types.

**Expected Task Outcomes**  
• Deploy an application on Minikube and expose it using a `ClusterIP` Service  
• Verify that the `ClusterIP` application is reachable from within the cluster by sending a request from another Pod using `kubectl exec`  
• Change the Service type to `NodePort` and access the application from a browser  
• Use `minikube tunnel` to test a `LoadBalancer` Service and access it through the address made available by Minikube  
• Explain the networking differences between `ClusterIP`, `NodePort`, and `LoadBalancer`  
• Write a short comparison describing what each Service type does and when it would be appropriate to use it  

**Resource Links**  
• Kubernetes Services: https://kubernetes.io/docs/concepts/services-networking/service/  
• Minikube service access: https://minikube.sigs.k8s.io/docs/handbook/accessing/  
• Minikube tunnel: https://minikube.sigs.k8s.io/docs/commands/tunnel/  
• kubectl reference: https://kubernetes.io/docs/reference/kubectl/  


### **Task 7: Introduction to AWS EKS**

**Task Description**  
Move from a local Kubernetes environment such as Minikube to a managed Kubernetes cluster on AWS. Learn the purpose of Amazon Elastic Kubernetes Service (EKS), create a cluster after reviewing the prerequisites and costs, configure access from your local machine, and deploy a simple Pod using `kubectl`.

**Expected Task Outcomes**  
• Explain the role of Amazon EKS and how a managed cloud Kubernetes cluster differs from a local Minikube cluster  
• Review the prerequisites and potential costs before creating an EKS cluster  
• Create an AWS EKS cluster using an appropriate documented method  
• Configure local access to the cluster and verify connectivity with `kubectl`  
• Deploy a simple Pod to the EKS cluster using `kubectl` commands and verify its status  

**Resource Links**  
• Amazon EKS User Guide: https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html  
• Getting started with Amazon EKS: https://docs.aws.amazon.com/eks/latest/userguide/getting-started.html  
• Connecting kubectl to an EKS cluster: https://docs.aws.amazon.com/eks/latest/userguide/create-kubeconfig.html  
• Kubernetes kubectl overview: https://kubernetes.io/docs/reference/kubectl/  


### **Task 8: Introduction to Observability**

**Task Description**  
Build the habit of inspecting an application's behaviour while it is running. Learn how CPU, memory, and disk resources relate to a Kubernetes Pod and what can happen when resource limits or available capacity are exceeded. Deploy a Pod, stream its logs while sending requests, inspect Pod- and node-level resource usage, and access a metrics endpoint through port forwarding.

**Expected Task Outcomes**  
• Explain how CPU, memory, and disk resources relate to a Kubernetes Pod  
• Describe what can happen when a Pod exceeds its memory or CPU limits, or when storage runs out  
• Deploy a Pod and stream its logs using `kubectl logs -f` while sending requests to the application  
• Use Kubernetes commands to inspect Pod details and understand Pod- and node-level resource usage  
• Use `kubectl port-forward` to expose a Pod's metrics endpoint locally and open the endpoint in a browser  
• Explain what the observed logs and resource metrics reveal about the application's runtime behaviour  

**Resource Links**  
• Kubernetes resource management for Pods and containers: https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/  
• Kubernetes logging: https://kubernetes.io/docs/concepts/cluster-administration/logging/  
• kubectl logs reference: https://kubernetes.io/docs/reference/kubectl/generated/kubectl_logs/  
• kubectl top reference: https://kubernetes.io/docs/reference/kubectl/generated/kubectl_top/  
• kubectl port-forward reference: https://kubernetes.io/docs/reference/kubectl/generated/kubectl_port-forward/  


---

## CY - Cybersecurity

### **Red Team Path**

The Red Team Path introduces offensive security concepts through structured, hands-on learning. Work through the rooms in order to build an understanding of the cyber kill chain, penetration-testing methodology, reconnaissance, network scanning, common web vulnerabilities, red-team engagements, and phishing awareness.

Complete all activities only within TryHackMe labs or other environments for which you have explicit authorisation. Keep notes on the commands used, the observations made, and the lessons learned.

### **Task 1: Cyber Kill Chain**

**Task Description**  
Explore the Cyber Kill Chain framework and understand the stages commonly used to describe an adversary's activity, from reconnaissance through actions on objectives. Learn how defenders can use the framework to recognise attacker behaviour and identify opportunities to disrupt an attack.

**Expected Task Outcomes**  
• Explain the purpose of the Cyber Kill Chain framework  
• Identify and describe its major phases: reconnaissance, weaponization, delivery, exploitation, installation, command and control, and actions on objectives  
• Understand how open-source intelligence (OSINT) supports reconnaissance  
• Explain how defenders can identify opportunities to detect, prevent, or disrupt activity at different stages of the kill chain  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Cyber Kill Chain: https://tryhackme.com/room/cyberkillchainzmt  


### **Task 2: Penetration Testing Fundamentals**

**Task Description**  
Learn the purpose, scope, and workflow of a penetration test. Understand how penetration testing differs from other security assessments, why authorisation and scope are essential, and how findings should be documented and communicated.

**Expected Task Outcomes**  
• Explain the purpose of a penetration test and how it differs from a vulnerability assessment  
• Identify the typical stages of a penetration-testing engagement  
• Understand the importance of scope, rules of engagement, authorisation, and responsible conduct  
• Recognise the role of evidence, impact assessment, and clear reporting in communicating findings  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Pentesting Fundamentals: https://tryhackme.com/room/pentestingfundamentals  


### **Task 3: Passive Reconnaissance**

**Task Description**  
Practise collecting information about a target from publicly available sources without directly interacting with the target's systems. Explore domain-registration information, DNS records, certificate transparency, subdomain discovery, and internet-exposed service search engines.

**Expected Task Outcomes**  
• Explain the difference between passive and active reconnaissance  
• Use `whois`, `dig`, and `nslookup` to gather and interpret domain information  
• Explore how certificate transparency logs and public sources can reveal subdomains  
• Understand how services such as Shodan can provide information about internet-exposed systems  
• Record findings clearly and distinguish verified facts from assumptions  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Passive Reconnaissance: https://tryhackme.com/room/passiverecon  


### **Task 4: Active Reconnaissance**

**Task Description**  
Learn how direct interaction with a system can reveal information about its availability, network path, exposed services, and web technologies. Practise the room's reconnaissance techniques in the provided lab environment and understand that active probing may be logged or detected.

**Expected Task Outcomes**  
• Explain how active reconnaissance differs from passive reconnaissance and why it may be detectable  
• Use browser Developer Tools to inspect relevant web-page information, headers, scripts, and certificates  
• Use `ping` to test reachability and understand the limitations of interpreting TTL values  
• Use `traceroute` or equivalent tools to examine network paths  
• Use `telnet` or `netcat` in the lab to inspect service responses and banners  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Active Reconnaissance: https://tryhackme.com/room/activerecon  


### **Task 5: Nmap Basic Port Scans**

**Task Description**  
Learn how Nmap discovers hosts and scans ports. Practise basic scan techniques in the authorised TryHackMe lab, then interpret the results to understand which ports are open, closed, or filtered and what those states suggest about a target's network services.

**Expected Task Outcomes**  
• Explain the purpose of Nmap in network discovery and port scanning  
• Perform the basic scans demonstrated in the room against the assigned lab target  
• Interpret common port states, including open, closed, and filtered  
• Understand at a high level how TCP connection scans and SYN scans differ  
• Record scan results and explain what they reveal about the lab target  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Nmap 01: https://tryhackme.com/room/nmap01  
• Nmap Reference Guide: https://nmap.org/book/man.html  


### **Task 6: Nmap Advanced Port Scans**

**Task Description**  
Build on basic scanning knowledge by exploring the more advanced Nmap scan techniques covered in the room. Learn how scan behaviour and packet flags affect the results, and practise interpreting the output in the provided lab environment.

**Expected Task Outcomes**  
• Explain the purpose of the advanced Nmap scan techniques covered in the room  
• Run the relevant scans against the assigned TryHackMe lab target  
• Compare the results of different scan types and explain why they may differ  
• Understand that network filtering, host configuration, and firewall behaviour can affect scan results  
• Document the commands used and the conclusions supported by the results  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Nmap 02: https://tryhackme.com/room/nmap02  
• Nmap Reference Guide: https://nmap.org/book/man.html  


### **Task 7: OWASP Top 10 2025 — Part 1**

**Task Description**  
Begin exploring the web application security risks covered in the OWASP Top 10 2025 learning rooms. Understand the vulnerability categories and scenarios presented in the room, and learn to recognise how weaknesses in web applications can affect confidentiality, integrity, and availability.

**Expected Task Outcomes**  
• Review the OWASP Top 10 2025 topics introduced in the room  
• Explain the vulnerability categories and examples covered by the exercises  
• Identify the underlying causes and potential impact of the demonstrated weaknesses  
• Complete the room's practical exercises only in the provided lab environment  
• Record key observations and defensive measures relevant to the topics studied  

**Resource Links**  
• TryHackMe — OWASP Top 10 2025: Part 1: https://tryhackme.com/room/owasptopten2025one  
• OWASP Top 10: https://owasp.org/www-project-top-ten/  


### **Task 8: OWASP Top 10 2025 — Part 2**

**Task Description**  
Continue studying the web application security topics covered by the second OWASP Top 10 2025 room. Work through the provided examples to understand how the relevant weaknesses arise, how their impact can be assessed, and what secure development practices help prevent them.

**Expected Task Outcomes**  
• Review the OWASP Top 10 2025 topics introduced in this room  
• Explain the causes and potential consequences of the vulnerabilities demonstrated  
• Complete the practical exercises in the assigned TryHackMe environment  
• Identify relevant prevention, validation, access-control, or configuration practices where applicable to the topics covered  
• Summarise the main lessons from the room in your own words  

**Resource Links**  
• TryHackMe — OWASP Top 10 2025: Part 2: https://tryhackme.com/room/owasptopten2025two  
• OWASP Top 10: https://owasp.org/www-project-top-ten/  


### **Task 9: OWASP Top 10 2025 — Part 3**

**Task Description**  
Complete the OWASP Top 10 2025 room sequence by exploring the remaining topics and practical scenarios presented in Part 3. Focus on understanding the security weaknesses, the conditions that make them possible, and the lessons developers and security testers can take from each exercise.

**Expected Task Outcomes**  
• Review the OWASP Top 10 2025 topics introduced in this room  
• Explain the relevant weaknesses, their likely impact, and the lessons demonstrated by the exercises  
• Complete the assigned practical activities in the TryHackMe lab  
• Identify defensive practices that address the issues covered in the room  
• Write a short summary of the key concepts learned across Parts 1, 2, and 3  

**Resource Links**  
• TryHackMe — OWASP Top 10 2025: Part 3: https://tryhackme.com/room/owasptopten2025three  
• OWASP Top 10: https://owasp.org/www-project-top-ten/  


### **Task 10: Red Team Fundamentals**

**Task Description**  
Understand the purpose and structure of a red-team engagement and how it differs from a conventional vulnerability assessment or penetration test. Explore engagement roles, objectives, adversary emulation, and the use of frameworks such as the Cyber Kill Chain to describe attacker behaviour.

**Expected Task Outcomes**  
• Explain what a red-team engagement is and what it aims to evaluate  
• Distinguish red teaming from vulnerability assessments and penetration testing  
• Identify the roles, stakeholders, objectives, and planning considerations involved in an engagement  
• Explain adversary emulation and the use of tactics, techniques, and procedures (TTPs)  
• Describe how a kill-chain framework can help organise and assess an engagement  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Red Team Fundamentals: https://tryhackme.com/room/redteamfundamentals  
• MITRE ATT&CK: https://attack.mitre.org/  


### **Task 11: Phishing Emails — Part 1**

**Task Description**  
Learn how to inspect suspicious emails and recognise common phishing indicators. Examine the evidence presented in the TryHackMe exercises, including sender details, links, attachments, and message content, to understand how phishing attempts can be identified and reported.

**Expected Task Outcomes**  
• Explain what phishing is and why it is used in social-engineering attacks  
• Inspect email sender details, message content, links, and attachments for suspicious indicators  
• Recognise common warning signs such as spoofed senders, misleading links, unexpected attachments, and urgent requests  
• Understand safe handling and reporting practices for suspicious emails  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Phishing Emails 1: https://tryhackme.com/room/phishingemails1tryoe  
• CISA — Recognize and Report Phishing: https://www.cisa.gov/secure-our-world/recognize-and-report-phishing  


### **Blue Team Path**

The Blue Team Path introduces defensive security operations, security monitoring, threat hunting, and endpoint security. Focus on understanding what defenders observe, how they investigate suspicious activity, and how security controls help detect and respond to threats.

### **Task 12: SOC Fundamentals**

**Task Description**  
Explore the role of a Security Operations Center (SOC) and how analysts monitor, investigate, and respond to security events. Learn about SOC responsibilities, common workflows, alert triage, and the tools used to support defensive operations.

**Expected Task Outcomes**  
• Explain the purpose and core responsibilities of a SOC  
• Understand common SOC roles and the general alert-investigation workflow  
• Distinguish security events, alerts, and incidents at a basic level  
• Explain why context, prioritisation, documentation, and escalation matter during investigations  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — SOC Fundamentals: https://tryhackme.com/room/socfundamentals  


### **Task 13: Introduction to SIEM**

**Task Description**  
Learn how Security Information and Event Management (SIEM) systems collect and analyse security logs from different sources. Explore how logs are used to search for activity, identify suspicious patterns, and support security investigations.

**Expected Task Outcomes**  
• Explain the purpose of a SIEM and the types of data it can collect  
• Understand how logs from different systems provide context during an investigation  
• Practise the searches, filters, and analysis activities demonstrated in the room  
• Explain how SIEM alerts can help analysts identify and investigate suspicious activity  
• Complete the activities and questions in the TryHackMe room  

**Resource Links**  
• TryHackMe — Introduction to SIEM: https://tryhackme.com/room/introtosiem  


### **Task 14: Threat Hunting Introduction**

**Task Description**  
Understand threat hunting as a proactive approach to searching for signs of malicious activity that may not have been detected by existing alerts. Explore the hunting mindset, the use of hypotheses, and the analysis of available security data to investigate suspicious behaviour.

**Expected Task Outcomes**  
• Explain what threat hunting is and how it differs from alert-driven investigation  
• Understand how a hypothesis can guide a threat-hunting investigation  
• Identify the role of logs, telemetry, and contextual evidence in hunting  
• Practise the investigation steps and analysis activities presented in the room  
• Document findings and explain how evidence supports or weakens a hypothesis  

**Resource Links**  
• TryHackMe — Threat Hunting Introduction: https://tryhackme.com/room/threathuntingintroduction  


### **Task 15: Introduction to Endpoint Security**

**Task Description**  
Learn how endpoint security helps protect devices such as workstations and servers. Explore the security controls and monitoring concepts introduced in the room, and understand how endpoint telemetry can help defenders detect suspicious activity and investigate potential compromise.

**Expected Task Outcomes**  
• Explain what an endpoint is and why endpoint security is important  
• Understand the purpose of endpoint protection and monitoring controls covered in the room  
• Recognise how endpoint activity can provide evidence during security investigations  
• Complete the practical activities and questions in the TryHackMe room  
• Summarise the defensive concepts learned and how they support detection and response  

**Resource Links**  
• TryHackMe — Introduction to Endpoint Security: https://tryhackme.com/room/introtoendpointsecurity  


### **Practical**

The practical section brings the learning paths together through hands-on web application security exercises. Work only within the intentionally vulnerable training application and the lab environment provided for this course. Document the issue investigated, the evidence observed, the impact, and the relevant mitigation.

### **Task 16: OWASP Juice Shop**

**Task Description**  
Explore OWASP Juice Shop, an intentionally vulnerable web application designed for security training. Investigate the application in the authorised lab environment, work through suitable challenges, and connect the vulnerabilities you observe to the web security concepts covered in the Red Team Path.

**Expected Task Outcomes**  
• Navigate the Juice Shop application and understand its purpose as a security training environment  
• Complete a selection of challenges appropriate to the course's learning objectives  
• Identify the vulnerability or security weakness demonstrated by each completed challenge  
• Document the steps taken, the evidence observed, and the potential impact  
• Where applicable, explain the defensive measures that would help prevent or mitigate the issue  
• Relate practical findings to the OWASP Top 10 topics studied earlier  

**Resource Links**  
• TryHackMe — OWASP Juice Shop: https://tryhackme.com/room/owaspjuiceshop  
• OWASP Juice Shop Project: https://owasp.org/www-project-juice-shop/  


### **Task 17: MARVEL Cybersecurity Red Team Lab**

**Task Description**  
Complete the practical exercise provided by the MARVEL Cybersecurity Red Team Lab. Use the techniques and concepts learned throughout the course to investigate the assigned lab environment, follow the exercise objectives, and document your approach and findings.

**Expected Task Outcomes**  
• Access and review the MARVEL Red Team Lab instructions  
• Identify the objective and scope of the assigned exercise before beginning  
• Apply relevant reconnaissance, scanning, and web-security concepts within the authorised lab  
• Record the tools used, steps taken, evidence collected, and conclusions reached  
• Summarise the security weaknesses or lessons demonstrated by the exercise and, where relevant, suggest mitigations  

**Resource Links**  
• MARVEL Cybersecurity Red Team Lab: https://28d33.github.io/Marvel-CLCY_L2-CY_RED-Lab/  
