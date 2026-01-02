pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/abhi2330/Online-food-.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-food-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh '''
                docker stop food || true
                docker rm food || true
                '''
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 --name food devops-food-app'
            }
        }
    }
}
