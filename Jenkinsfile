pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t wojtek0/my-app:latest .'
            }
        }

        stage('Docker Push') {
            steps {
                sh 'docker login -u wojtek0 -p YOUR_PASSWORD'
                sh 'docker push wojtek0/my-app:latest'
            }
        }
    }
}