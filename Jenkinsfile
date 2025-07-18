pipeline {
    agent {
        docker {
            image 'node:18'
            args '-v /root/.npm:/root/.npm' // optional: cache npm between builds
        }
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build' // if you have a build script
            }
        }

        stage('Test') {
            steps {
                sh 'npm test' // optional if tests are defined
            }
        }

        stage('Deploy') {
            steps {
                echo 'Add deployment steps here'
            }
        }
    }
}

