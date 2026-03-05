pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/your-repo/frontend-project.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the frontend project"
            }
        }

        stage('Test') {
            steps {
                echo "Testing the application"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying application"
                sh 'cp index.html /var/www/html/'
            }
        }
    }
}