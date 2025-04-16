pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://uvishnuvardhan30001.github.io/portfolio/', credentialsId: 'github-creds'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('portfolio-html')
                }
            }
        }
    }
}
