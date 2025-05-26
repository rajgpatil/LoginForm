pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/rajgpatil/LoginForm.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage - nothing to build for static HTML"
            }
        }

        stage('Test') {
            steps {
                echo "Test stage - you can add HTML validators here"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying..."
                // Simulate deploy: adjust this line if you're copying to a real server
                sh 'cp index.html /path/to/deployment/folder/'
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
