
pipeline {
    agent { label "Dev"};

    stages {
        stage('Code') {
            steps {
                git url: 'https://github.com/abhi2330/Online-food-.git',
                    branch: 'main'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'docker build -t online-food:latest .'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Docker image...'
                sh 'docker image inspect online-food:latest'
            }
        }

        stage('Push to Docker Hub') {
            steps {
                withCredentials([usernamePassword(
                    credentialsId: 'JenkinsCred',
                    usernameVariable: 'dockerHubUser',
                    passwordVariable: 'dockerHubPass'
                )]) {
                    sh '''
                        echo "$dockerHubPass" | docker login \
                            -u "$dockerHubUser" --password-stdin

                        docker image tag online-food:latest \
                            "$dockerHubUser/online-food:latest"

                        docker push "$dockerHubUser/online-food:latest"

                        docker logout
                    '''
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh '''
                    docker rm -f online-food || true

                    docker run -d \
                        --name online-food \
                        --restart unless-stopped \
                        -p 8081:80 \
                        online-food:latest
                '''
            }
        }
    }
}
