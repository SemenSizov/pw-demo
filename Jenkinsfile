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
      stage('Run tests'){
        steps {
          bat 'npm test'
        }
        post {
          always {
            arhiveArtifacts(artifacts: 'playwright-report', allowEmptyArchive: true)
          }
        }
      }
  }
}