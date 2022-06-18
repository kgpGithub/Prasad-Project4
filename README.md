# Prasad-Project4
[![CircleCI](https://dl.circleci.com/status-badge/img/gh/kgpGithub/Prasad-Project4/tree/main.svg?style=svg)]
(https://dl.circleci.com/status-badge/redirect/gh/kgpGithub/Prasad-Project4/tree/main)

## Project Overview

In this project, i have applied the skills that i have acquired in this course to operationalize a Machine Learning Microservice API. 

i have  given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. I read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests the ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

My project goal is to operationalize the working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Tested the project code using linting
* Completed a Dockerfile to containerize this application
* Deployed the containerized application using Docker and make a prediction
* Improve  log statements in the source code for this application
* Configured Kubernetes and created a Kubernetes cluster
* Deployed a container using Kubernetes and made a prediction
* Uploaded a complete Github repo with CircleCI to indicate that your code has been tested
 
 ### Files contained

.circleci/config.yml contains circle ci jobs and builds
Docker_out.txt - contains terminal output from running ./run_docker.sh
Kubernetes_out.txt - contains terminal output from running ./run_kubernetes.sh
Dockerfile - contains instructions to build docker image
Makefile - installs the dependencies for the project
app.py - source code which also contains an additional prediction log statement
Make_prediction.sh - sends input data to the containerised port via the port listed
Requirements.txt - includes project dependencies
Run_docker.sh - contains instructions to run and build the docker image outlined in the Dockerfile
Run_kubernetes.sh - deploys the application to kubernetes
Upload_docker.sh - uploads the built image to docker

### Setup the Environment

Change to working directory
python3 -m venv ~/.devops
source ~/.devops/bin/activate
make install <- to install dependencies
install hadolint <-  sudo wget -O ~/.devops/bin/hadolint https://github.com/hadolint/hadolint/releases/download/v1.16.3/hadolint-Linux-x86_64
install virtualbox <-- curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
                   <-- sudo install minikube-linux-amd64 /usr/local/bin/minikube


### Running app.py

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl
