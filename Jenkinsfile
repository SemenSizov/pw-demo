pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
            sh '/usr/bin/npm ci'
          }
        }
      stage('Run tests'){
        steps {
          sh '/usr/bin/npm test'
        }
      }
  }
}