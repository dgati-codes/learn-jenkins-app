pipeline {
    agent any

    stages {
        agent {
            docker{
                image 'node:18-alpine'
                reuseNode true
            }
        }
        stage('Build') {
            steps {
                '''
                ls -la
                node --version
                npm --version
                npm ci
                npm run build
                ls -la
                
                
                '''
            }
        }
    }
}
