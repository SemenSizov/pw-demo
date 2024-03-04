pipeline {
    agent any
    stages {
        stage('Install dependencies') {
            steps {
                bat 'npm ci'
            }
        }
        stage('Install Playwright') {
            steps {
                bat 'npx playwright install --with-deps'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         echo 'Deploying....'
        //     }
        // }
    }
}