For Maven project demo application, implementing continues deployment to docker/k8 environemnt

Created sample demo project using https://start.spring.io/

Tools:
GitHub source code management
Jenkins build server
Docker environment

Implementation Process:
- Build project using maven
- Create Docker image
- Run application as Docker container

The Dockerfile and Jenkinsfile are in github source repository itself.
Create webhook from github to jenkins for continues deployment process.
