pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout from Git Jenkinsfile'
            }
        }
        stage('Build') {
            steps {
                echo 'Build stage from Jenkinsfile'
            }
        }
        stage('Test') {
            steps {
                echo 'Test stage from Jenkinsfile'
            }
        }
    }

    post {
        success {
            echo 'Build Successful'
        }
        failure {
            echo 'Build Failed'
        }
    }
}
