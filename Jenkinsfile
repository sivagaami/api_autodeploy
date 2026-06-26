pipeline {
    agent any
environment {
        PATH = "/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin"
    }

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

       stage('Docker Build') {
            steps {
                sh 'docker build -t devopsfirstapi:latest .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name devopsfirstapi-container -p 3000:3000 devopsfirstapi:latest'
            }
        }
    }
}        