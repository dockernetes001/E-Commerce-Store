pipeline {
    agent any
    environment {
        STAGING_SERVER = 'user@vue-nginx-1'
        REMOTE_PATH = '/var/www/html'
    }
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/ezbrush/E-Commerce-Store'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install' // o 'yarn install'
            }
        }
        stage('Code Quality') {
            steps {
                sh 'npm run lint || true'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Test') {
            steps {
                sh 'npx cypress run --component --headless'
            }
        }
        stage('Archive Build') {
            steps {
                archiveArtifacts artifacts: 'dist/**', fingerprint: true
            }
        }
        stage('Deploy to Staging') {
            steps {
                sshagent(['vue-nginx-1']) {
                 sh "scp -o StrictHostKeyChecking=no -r dist/* ${STAGING_SERVER}:${REMOTE_PATH}/"
                }
            }
        }
        stage('Validate Deployment') {
            steps {
                sh 'sleep 10'
                sh 'curl --fail http://vue-nginx-1:80 || exit 1'
            }
        }
    }
}
