pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
          withNPM() {
            sh 'npm ci'
          }
        }
      }
      stage('Run tests'){
        steps {
        withNPM() {

          sh 'npm test'
        }
        }
      }
  }
}