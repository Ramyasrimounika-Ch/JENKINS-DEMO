pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Ramyasrimounika-Ch/JENKINS-DEMO'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t 2023bcs0223mounika/2023bcs0223 .'
            }
        }

        stage('Login DockerHub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', usernameVariable: 'USER', passwordVariable: 'PASS')]) {
                    sh 'echo $PASS | docker login -u $USER --password-stdin'
                }
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push 2023bcs0223mounika/2023bcs0223'
            }
        }

    }
}