# Project 1

Demonstration of Deployment of cloned Reddit application on a cluster using minikube and Docker.

---------------
# Project 2

Demonstration of Deployment of cloned Reddit application on a Kubernetes cluster using kubernetes and Docker also we will monitor the application using Promeatheus and visualization of monitored data through Graffana.
<br>

In this project we will use following aws services: - <br>
1. Elastic Container Repository (ECR) <br>
2. EC2 instance
3. Virtual Private Cloud (VPC) <br>
4. Elastic IP (EIP) <br>
5. Elastic Kubernetes Service (EKS) <br>

------------------
# Important Diagrams

## 1. Kubernetes Architecture

![Kubernetes-Architecture](https://user-images.githubusercontent.com/102405310/235336458-84b0fe94-42bb-4285-a45f-0ef86b0223e5.png)
<br>
-----------------
## 2. Connection between Nodeport, Port and Target Port
-----------------

![2bVEz](https://user-images.githubusercontent.com/102405310/235336875-bfcec6f4-d605-45bb-ae29-ea5624038a36.png)

------------------
## 3. Cluster management
------------------

<img width="1096" alt="Screenshot 2023-04-24 at 2 22 27 PM" src="https://user-images.githubusercontent.com/102405310/235337723-1f94b645-f7e3-4184-8cac-0ebb1eb6aba3.png">

-------------------
## 4. AWS VPC Architecture
-------------------
![VPC-Network-Engineers-Part-1-1](https://user-images.githubusercontent.com/102405310/235347335-be9e5aa8-7328-4138-ab71-eea34a78e8e2.png)



-----------------
## Dockerfile Basics

<p> Dockerfile is basically a textfile. It contains some set of instructions.</p>
<p> Used for Automation of creation of Docker Image. </p>

### Dockerfile Components

<ul> 
<li> FROM: - For Base Image. This command must be on top of the Dockerfile. </li>
<li> RUN: - To execute command inside the container. </li>
<li> MAINTAINER: - Author/Owner/Description </li>
<li> COPY: - Copy files from local system. We need to provide Source(local machine) & Destination(container base image). </li>
<li> ADD: - Similar to COPY but, it provides a feature to download files from internet, also we can untar archive or extract. </li>
<li> EXPOSE: - To expose ports such as port 8080 for tomcat, port 80 for nginx etc. </li>
<li> WORKDIR: - To set working directory for a container. </li>
<li> CMD: - Execute command but during container creation </li>
<li> ENTRYPOINT: - Similar to CMD, but has a higher priority over CMD. </li>
<li> ENV: -  For configuring environment variables.</li>
</ul>

![dockercheatsheet7](https://user-images.githubusercontent.com/102405310/235626290-36c4349e-3815-42ac-a6dd-3b34952821a1.png)



-----------------------------
## Docker CheatSheet
![dockercheatsheet8](https://user-images.githubusercontent.com/102405310/235626278-5347187e-4060-4cee-82b0-a1c410f3b914.png)







 
