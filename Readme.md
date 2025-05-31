# Practical 7: Jenkins Shared Library for Node.js Applications

## Objective

The objective of this practical exercise was to create a reusable Jenkins Shared Library that centralizes common pipeline logic for Node.js applications. The shared library includes steps for installing dependencies, running tests, building Docker images, and pushing to DockerHub. This approach promotes consistent builds, reduces copy-paste errors, and simplifies maintenance across multiple projects.

## Steps Involved 

### 1. Create the Shared Library Repository Structure

![alt text](images/repo.png)

### 2. Create Shared Library Files

![alt text](images/files.png)

### 3. Create Example Node.js Application

![alt text](images/node_app.png)

Example Jenkinsfile

![alt text](images/jenkins.png)

### 4. Configure Jenkins

Navigate to "Manage Jenkins" > "Configure System"

![alt text](images/global.png)

Add a new Global Pipeline Library:

Name: shared-library

Default version: main

Retrieval method: "Modern SCM" > "Git"

Project repository URL: Your Git repository URL

![alt text](images/golbal.png)

### 5. Create Jenkins Pipeline Job

Create a new Pipeline job in Jenkins

![alt text](images/pipeline.png)

Configure source code management to pull from your application repository

Set the Jenkinsfile path

Path set as node-app/Jenkinsfile

![alt text](images/scriptpath.png)

![alt text](images/pipeline2.png)

Run the pipeline

