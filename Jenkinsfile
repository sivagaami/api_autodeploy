pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code cloned from GitHub'
            }
        }
        stage('Git Check') {
            steps {
                sh 'git --version'
            }
        }

        stage('Docker Check') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }

    }
}
