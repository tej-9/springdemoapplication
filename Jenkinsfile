pipeline {
    agent any

    stages {
        stage('Clone Project') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            }
          }
        stage('Build Docker image with BUILD_NUMBER') {
            steps {
               // Build using Dockerfile
               sh label: '', script: 'docker build -t demo:$BUILD_NUMBER .'
            }
         }
        stage('Run application Docker container') {
            steps {
              // Run container
              sh label: '', script: 'docker run -p 8080:8080 demo:$BUILD_NUMBER'
            }
         }
        }
        post {
        always {
            cleanWs()
        }
    }
    }
}
