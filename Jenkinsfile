pipeline {
    agent none
    stages {
        stage('Build') {
            agent {
                docker {
                    image 'maven:3.8.6-eclipse-temurin-17-alpine'
                    args '-v $HOME/.m2/:/root/.m2/'
                }
            }
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Deploy') {
            agent any
            steps {
                sh 'docker run -d -p 8080:8080 --name deploy-docker-sample localhost:5000/deploy-docker-sample:0.0.1-SNAPSHOT'
            }
        }
    }
}