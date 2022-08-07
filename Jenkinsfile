pipeline {
    agent {
        docker {
            image 'maven:3.8.6-eclipse-temurin-17-alpine'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}