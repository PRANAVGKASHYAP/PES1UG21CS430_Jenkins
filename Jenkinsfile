pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
               git branch: 'main',
               url: 'https://github.com/PRANAVGKASHYAP/PES1UG21CS430_Jenkins.git'  // Replace with your Git repository URL
            }
        }
        stage('Build') {
            steps {
                build 'PES1UG21CS355-1'
                sh 'g++ hello2.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
