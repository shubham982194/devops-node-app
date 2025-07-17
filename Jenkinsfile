pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/shubham982194/devops-node-app.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh 'node app.js &'
                echo 'App started'
            }
        }
    }
}

