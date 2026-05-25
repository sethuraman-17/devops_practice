pipeline {
    agent any

    stages {

        stage('Clone Info') {
            steps {
                bat 'echo Cloning Repository'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Building Application'
            }
        }

        stage('Test') {
            steps {
                bat 'echo Running Tests'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploying Application'
            }
        }
    }
}