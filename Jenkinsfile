pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/ug-devops/spring-petclinic.git', branch: 'main', credentialsId: 'b86b14c1-4f74-45b4-9154-81eb6e59f126'
            }
        }
        stage('Build') {
            steps {
                sh './mvnw clean install'
            }
        }
        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }
    }
}

