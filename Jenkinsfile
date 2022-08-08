pipeline {
    agent {
        docker {
            image 'maven:3.8.6-eclipse-temurin-17-alpine'
            args '-u root -v $HOME/.m2/:/root/.m2/'
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