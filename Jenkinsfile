pipeline {
    agent { docker { image 'python:3.11.4-alpine3.18' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
