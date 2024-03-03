pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
          withNPM(npmrcConfig: 'MyNpmrcConfig') {
            sh 'npm ci'
          }
        }
      }
      stage('Run tests'){
        steps {
        withNPM(npmrcConfig: 'MyNpmrcConfig') {

          sh 'npm test'
        }
        }
      }
  }
}