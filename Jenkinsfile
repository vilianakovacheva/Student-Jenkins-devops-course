pipeline {
    agent any
    stages {
        stage('NPM install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run npm audit tests') {
            steps {
                sh 'npm audit'
            }
        }
        stage('Run integration tests') {
            steps {
                sh 'npm run test'
            }
        }
        stage('Deploy to STAGING') {
            steps {
                echo 'Deploying to staging'
            }
        }
        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deploying to production'
            }
        }
    }
}
