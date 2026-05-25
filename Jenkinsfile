pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                bat 'echo Cloning Source Code'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sethu17/my-nginx-app:v1 .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push sethu17/my-nginx-app:v1'
            }
        }
    }
}