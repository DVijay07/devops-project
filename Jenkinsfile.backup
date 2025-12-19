pipeline {
    agent any
    stages {
        stage('Fetch Code') {
            steps {
                git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/DVijay07/devops-project.git'
            }
        }
        stage('Build Image') {
            steps {
                sh 'docker build -t my-final-app .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker stop deepak-web-container || true'
                sh 'docker rm deepak-web-container || true'
                sh 'docker run -d --name deepak-web-container -p 8081:80 my-final-app'
            }
        }
    }
}