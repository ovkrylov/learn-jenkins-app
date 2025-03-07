pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                agent {
                    docker {
                        image 'node:18-alpine'
                    }
                }
                sh '''
                    npm ci
                    npm run build
                '''
            }
        }
    }
}