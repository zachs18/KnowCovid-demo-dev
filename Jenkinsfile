pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'DOCKER_HOST="127.0.0.1:2375" docker-compose up -d --build'
            }
            post {
                success {
                    echo 'Build successful. Now archiving...'
                    
                }
            }
        }
    }
}
