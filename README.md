# Kidney-Failure-Detection

Here, I have created a deep learning model to classify whether a kidney has stones or not. I utilized the VGG16 model, and the accuracy of this model is approximately 60%.



## Workflows

1. Update config.yaml
2. Update params.yaml
3. Update the entity
4. Update the configuration manager in src config
5. Update the components
6. Update the pipeline 
7. Update the main.py
8. Update the dvc.yaml


# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/niloycste/Kidney-Failure-Detection
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
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


### Data Version Control(DVC)

We use DVC to track our data and pipeline so that we dont need to do the same task again and again. here we track our pipeline using dvc
Anyone interested can go through this [link](https://dvc.org/doc)

1. dvc init
2. dvc repro
3. dvc dag


## MLflow

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/niloycste/Kidney-Failure-Detection.mlflow \
MLFLOW_TRACKING_USERNAME=niloycste \
MLFLOW_TRACKING_PASSWORD=55343c50b515f85d83d1bbecdf5e45f6664231d3 \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/niloycste/Kidney-Failure-Detection.mlflow

export MLFLOW_TRACKING_USERNAME=niloycste

export MLFLOW_TRACKING_PASSWORD=55343c50b515f85d83d1bbecdf5e45f6664231d3

```

## Final Output 
 <img src = "images/normal.png" width="" height="">
  <img src = "images/tumor.png" width="" height="">


  [Click here to watch the video](https://youtu.be/G_oyTUV9P10)


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
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken

	
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


  


