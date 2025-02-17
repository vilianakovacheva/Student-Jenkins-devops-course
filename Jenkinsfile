pipeline {
    agent any
    stages {
        stage('NPM install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run integration tests') {
            steps {
                sh 'npm run test'
            }
        }
    }
}
