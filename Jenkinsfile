pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {

                sh '''
                    npm ci
                    npm run build
                '''
            }
        }
    }
}