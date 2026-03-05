pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Ramyasrimounika-Ch/JENKINS-DEMO.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the project"
            }
        }

        stage('Test') {
            steps {
                echo "Testing the project"
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment successful"
            }
        }
    }
}
