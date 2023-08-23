pipeline {
    agent any
    options {
        // Timeout counter starts AFTER agent is allocated
        timeout(time: 100000, unit: 'SECONDS')
    }
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from the version control repository
                // (e.g., Git)
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                // Build your application (e.g., compile code, generate artifacts)
                echo 'build triggered automaticallu from webhook on commit from local repo'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests on your application
                echo 'your-test-command'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your application to a staging environment
                echo 'your-deploy-command'
            }
        }
        
        stage('Promote to Production') {
            steps {
                // Promote the application to production if tests pass in the staging environment
                echo 'your-promote-command'
            }
        }
    }
    
    post {
        success {
            // Clean up or notify on successful pipeline execution
            echo 'Pipeline executed successfully!'
        }
        failure {
            // Perform actions on pipeline failure (e.g., notifications)
            echo 'Pipeline failed!'
        }
    }
}
