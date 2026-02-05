pipeline {
    agent any

    // Environment block is where you define variables for the whole pipeline
    environment {
        APP_NAME = "Jenkins-Study-Project"
        OWNER = "Naresh"
    }

    stages {
        stage('Initialize') {
            steps {
                // In Groovy, we use ${} to print a variable inside a string
                echo "Starting build for ${APP_NAME}..."
                echo "Managed by: ${OWNER}"
            }
        }

        stage('Build & Test') {
            steps {
                echo "Running build for ${APP_NAME} version 1.0"
                sh 'grep -i "Jenkins" index.html'
            }
        }
    }

    post {
        success {
            echo "Successfully finished ${APP_NAME}! Great work, ${OWNER}."
        }
    }
}