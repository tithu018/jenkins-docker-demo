pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/tithu018/jenkins-docker-demo.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh 'ls -la'
            }
        }

        stage('Test') {
            steps {
                sh 'echo "Running tests..."'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-docker-demo:latest .'
            }
        }
    }
}
