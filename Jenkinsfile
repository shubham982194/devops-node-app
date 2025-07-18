pipeline {
    agent {
        docker {
            image 'node:18'
            args '-v /root/.npm:/root/.npm'
        }
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App (optional)') {
            steps {
                sh 'node app.js' // only if you want to run it in Jenkins
            }
        }
    }
}

