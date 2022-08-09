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
    }
}