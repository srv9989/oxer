pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/srv9989/oxer.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t mywebapp .'
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d -p 8080:80 --name mywebapp-container mywebapp'
                }
            }
        }
    }
}
