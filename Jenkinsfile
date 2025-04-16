pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'https://github.com/uvishnuvardhan30001/portfolio.git', credentialsId: 'github-creds'
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
