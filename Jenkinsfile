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
            sh 'mkdir -p deploy && cp index.html deploy/'
            archiveArtifacts artifacts: 'deploy/index.html', fingerprint: true
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
