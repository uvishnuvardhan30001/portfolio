pipeline {
    agent any

    environment {
        IMAGE_NAME = 'mrvishnu27/portfolio'
        DOCKER_CREDENTIALS_ID = 'dockerhub'
    }

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/uvishnuvardhan30001/portfolio.git', branch: 'main'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("${IMAGE_NAME}:latest")
                }
            }
        }

        stage('Push to Docker Hub') {
            steps {
                script {
                    docker.withRegistry('https://index.docker.io/v1/', "${DOCKER_CREDENTIALS_ID}") {
                        docker.image("${IMAGE_NAME}:latest").push()
                    }
                }
            }
        }
    }
}
