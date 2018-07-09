# springboot-hello-world

An insanely simple example of springboot

All I did here is very simple. It was just a test for deploying a CI/CD pipeline with the following flow:

PC -> Github -> Jenkins -> Docker -> Kubernetes

That's basically it.

## Running the code
---
The entire project can be run using docker.

To build the project, kindly run

> mvn package

This would build the entire project into a docker image due to the aid of the dockerfile-maven-plugin from spotify which allows one to bind the docker build and push process to a maven build process.

## Building with Jenkins
---
 
 A [Jenkinsfile](Jenkinsfile) has been added to enable one do the pipeline build on Jenkins automatically once a pull from Github is done.
 
 ## Deploying to Kubernetes
 ---
 
 A kubernetes file has been added which will setup the replicas and start the service automatically.
 
 To create the deployment and service, you'd be needing two things to test locally:


 minikube
   - A local kubernetes node 
   
 kubectl
   - The kubernetes command line tool
   
   
 Once both are setup, you can deploy it using the command below:
 
 > kubectl create -f [kubernetes.yml](kubernetes.yml)
 
 A load balancer setup was done so a cloud provider (AWS, Google Cloud) or a local ingress setup would be needed to get access to the service.
 
 ## FAQ
 
None at the moment. 
