# US VISA APPLICATION STATUS

ABOUT DATASET -
The dataset is sourced from Kaggle.
Source of data -> https://www.kaggle.com/datasets/jboysen/us-perm-visas

This repo aims to showcase two things
1. Business Problem -> Develop a model to predict visa decisions based on employee/employer/wage?
2. Develop an E2E project with modular coding that can be containerized with docker and deployed on the AWS cloud using GitHub actions.



# Local Setup

Follow the below steps to run the code.


## Step1 : commands to create venv
conda create -n visa python=3.8 -y #n installs in c drive
conda activate visa

## Step2 : installing requirements.txt
pip3 install -r requirements.txt

## Mongo DB setup
create an account on Mongodb and create a collection over there. Generate a connection string. Set below environment variable
export MONGODB_URL="<mongodb url>"

## Step4: To run the file locally
export AWS_ACCESS_KEY_ID =<>
export AWS_SECRET_ACCESS_KEY=<>
python demo.py




# AWS-CICD-Deployment-with-Github-Actions

EC2 access: It is a virtual machine

ECR: Elastic Container registry to save your docker image in aws

1. Create an account on AWS. Login to AWS console.

2. Create IAM user(us-visa) for deployment. Create a secret key and access key for the IAM user. Download the CSV file

3. Create a ECR registry(usvisa) on AWS (666711044981.dkr.ecr.us-east-1.amazonaws.com/usvisa)

4. Create EC2 Instance (usvisa-machine) - 32Gb volume 8 Gb Ram. Add 7080 custom TCP port

5. Connect to the instance. Update the packages
sudo apt-get update -y
sudo apt-get upgrade

6. Install docker on the instance

curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo usermod -aG docker ubuntu
newgrp docker


7. Setup GitHub secrets:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_DEFAULT_REGION
ECR_REPO




