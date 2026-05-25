pipeline {
    agent any

    environment {
        DOCKER_HUB_CREDS = credentials('dockerhub-creds')
    }

    stages {

        stage('Clone') {
            steps {
                bat 'echo Cloning Source Code'
            }
        }

        stage('Docker Login') {
            steps {
                bat 'docker login -u %DOCKER_HUB_CREDS_USR% -p %DOCKER_HUB_CREDS_PSW%'
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