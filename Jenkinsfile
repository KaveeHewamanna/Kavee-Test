pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Application Build Successful'
            }
        }

        stage('Test') {
            steps {
                bat 'if exist index.html (echo Test Passed) else (exit /b 1)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Application Deployed Successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed. Check error'
        }
    }
}
