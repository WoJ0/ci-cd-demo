pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building app...'
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t my-app .'
            }
        }
    }
}