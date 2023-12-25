# End to End Text Summarization

## Overview
End to End Text Summarization is a project that leverages Natural Language Processing (NLP) techniques to automate the extraction of key information from large amounts of text data. The project utilizes the Pegasus model for implementation, providing an effective and efficient solution for creating concise summaries of lengthy textual content.

## Why Text Summarization?

Processing vast amounts of text data manually can be time-consuming, and in many cases, it's not feasible to read through extensive documents to extract essential information. The End to End Text Summarization project addresses this challenge by reducing reading time and presenting a shortened version of the original text.

## Features
- Automated Summarization: The project offers an end-to-end solution for automated text summarization.
- NLP Techniques: Leveraging state-of-the-art NLP techniques, including the Pegasus model, for effective summarization.
- CI/CD Pipeline: A continuous integration and continuous deployment (CI/CD) pipeline ensures seamless automation, testing, and deployment of the summarization model.

## CI/CD Pipeline
The project includes a CI/CD pipeline to automate the testing and deployment processes. The pipeline comprises the following steps:
Linting: Code linting ensures adherence to coding standards.
1. Unit Tests: Execute unit tests to validate the functionality of the summarization model.
2. Integration Tests: Verify the integration of the model with the overall system.
3. Deployment: Deploy the summarization model to a designated environment.

The CI/CD pipeline is triggered automatically upon changes to the main branch.


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/rkstu/text-summarizer-using-NLP.git
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n summary python=3.8 -y
```

```bash
conda activate summary
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up you local host and port
```


```bash
Author: Rahul Kumar
Data Scientist
Email: rkmailcode@gmail.com

```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: {URL}

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app
