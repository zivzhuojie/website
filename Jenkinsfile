pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from the repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build steps (if any) - For an HTML project, this may involve minifying, bundling, etc.
                sh 'npm install'  // Example build command
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the HTML project to a web server
                sh 'rsync -avz ./dist/ user@example.com:/var/www/html'  // Example deploy command
            }
        }
    }

    post {
        always {
            // Cleanup or notification steps can go here
        }
    }
}
