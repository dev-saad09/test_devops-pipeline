pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.build('node-app')
                }
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                kubectl apply -f deployment.yaml
                '''
            }
        }
    }
}
