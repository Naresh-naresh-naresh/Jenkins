pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // This pulls the latest code from your GitHub repo
                checkout scm 
            }
        }

        stage('Build & Lint') {
            steps {
                echo 'Checking HTML syntax... 🏗️'
                // We just 'echo' for now to simulate a build
                sh 'ls -lh' 
            }
        }

        stage('Test') {
            steps {
                echo 'Verifying content... 🧪'
                // This checks if your <h1> tag actually exists in the file
                sh 'grep -i "Jenkins" index.html' 
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Staging Environment... 🚀'
                // In a real job, this would move files to a web server
                echo 'Application is live at http://itqa-automation.runwayci.com'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up the workspace... 🧹'
        }
        success {
            echo 'Build Successful! Great job, Naresh.'
        }
        failure {
            echo 'Build Failed. Check your index.html for errors.'
        }
    }
}
