pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java code'
                bat 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Java program'
                bat 'java Hello'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline Successful'
            archiveArtifacts artifacts: '*.class', fingerprint: true
        }
        failure {
            echo 'CI Pipeline Failed'
        }
    }
}
