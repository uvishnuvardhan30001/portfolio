pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/my-html-project.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-html-app')
                }
            }
        }
    }
}
