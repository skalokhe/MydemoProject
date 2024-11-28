pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'your-branch-name', url: 'https://your-repo-url.git'
            }
        }
        stage('Run Docker Compose') {
            steps {
                script {
                    sh 'docker-compose up -d'
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}