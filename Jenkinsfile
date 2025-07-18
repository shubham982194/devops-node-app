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
                sh 'node -v && npm -v'
                sh 'npm install'
            }
        }
    }
}

