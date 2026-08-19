pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code from GitHub...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Starting build stage...'
                bat 'if not exist Dockerfile exit /b 1'
                echo 'Build stage completed successfully.'
            }
        }

        stage('Test') {
            steps {
                echo 'Starting test stage...'
                bat 'if not exist README.md exit /b 1'
                echo 'Test stage completed successfully.'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully.'
        }

        failure {
            echo 'Pipeline failed. Check Console Output.'
        }
    }
}
