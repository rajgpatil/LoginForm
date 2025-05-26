pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/rajgpatil/LoginForm.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage - no actual build for static HTML"
            }
        }

        stage('Test') {
            steps {
                echo "Testing HTML (optional for static site)"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to web server (simulated)"
                sh 'cp index.html /var/www/html/'  // Adjust as needed
            }
        }
    }

    post {
        success {
            echo "Deployment successful"
        }
        failure {
            echo "Deployment failed"
        }
    }
}
