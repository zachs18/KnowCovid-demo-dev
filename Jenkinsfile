pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker-compose up -d --build --DOCKER_HOST=127.0.0.1:2375'
            }
            post {
                success {
                    echo 'Build successful. Now archiving...'
                    
                }
            }
        }
    }
}
