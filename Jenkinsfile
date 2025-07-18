pipeline {
    agent {
        docker {
            image 'node:18'         // runs everything inside official Node.js image
            args '-v /root/.npm:/root/.npm' // optional: for npm caching
        }
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'node -v'
                sh 'npm -v'
                sh 'npm install'
            }
        }
    }
}

