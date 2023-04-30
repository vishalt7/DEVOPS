# Reddit Clone App on Kubernetes
This project demonstrates how to deploy a Reddit clone app on Kubernetes and expose it to the world using Minikube as the cluster.

## Prerequisites
Before you begin, you should have the following tools installed on your local machine: 

- Docker
- Minikube cluster ( Running )
- kubectl
- Git

# For Docker Installation
sudo apt-get update <br>
sudo apt-get install docker.io -y <br>
sudo usermod -aG docker $USER && newgrp docker <br>

---------------
minikube.sh
---------------
# For Minikube & Kubectl
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64  <br>
sudo install minikube-linux-amd64 /usr/local/bin/minikube  <br>

sudo snap install kubectl --classic <br>
minikube start --driver=docker <br>


-----------------
aws cli
----------------
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"  <br>
unzip awscliv2.zip  <br>
sudo ./aws/install  <br>


-----------------------------
CloudFormation URL for creating VPC stack
-----------------------------
https://amazon-eks.s3.us-west-2.amazonaws.com/cloudformation/2020-06-10/amazon-eks-vpc-private-subnets.yaml


--------------------------
eksctl
--------------------------
ARCH=amd64
PLATFORM=$(uname -s)_$ARCH

curl -sLO "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$PLATFORM.tar.gz"

tar -xzf eksctl_$PLATFORM.tar.gz -C /tmp && rm eksctl_$PLATFORM.tar.gz

sudo mv /tmp/eksctl /usr/local/bin

--------------------------
kubectl
--------------------------
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

kubectl version --client


--------------------------
aws-iam-authenticator
--------------------------
curl -Lo aws-iam-authenticator https://github.com/kubernetes-sigs/aws-iam-authenticator/releases/download/v0.5.9/aws-iam-authenticator_0.5.9_linux_amd64

chmod +x ./aws-iam-authenticator

mkdir -p $HOME/bin && cp ./aws-iam-authenticator $HOME/bin/aws-iam-authenticator && export PATH=$PATH:$HOME/bin

echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc

aws-iam-authenticator help


------------------------
Create an EKS cluster
------------------------
eksctl create cluster -f cluster.yaml --kubeconfig=~/.kube/config

aws eks --region ap-south-1 update-kubeconfig --name EKS-Demo-Cluster


------------------------
Delete an EKS cluster
------------------------

eksctl delete cluster --region=ap-southeast-1 --name=EKS-Demo-Cluster