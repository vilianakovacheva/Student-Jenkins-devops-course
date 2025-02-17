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
        stage('Approval for Production Deployment') {
            steps {
                script {
                    input message: 'Proceed with production deployment?', ok: 'Deploy'
                }
            }
        }
        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deploying to production'
            }
        }
    }
}
