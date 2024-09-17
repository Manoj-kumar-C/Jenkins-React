pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Deploy') {
            steps {
                // Add your deploy steps here (e.g., using Vercel CLI)
                sh 'npx vercel --prod --token $VERCEL_TOKEN'
            }
        }
    }
}
