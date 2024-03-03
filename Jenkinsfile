pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
          withNPM(npmrcConfig: 'my-custom-nprc') {
            sh 'npm ci'
          }
        }
      }
      stage('Run tests'){
        steps {
        withNPM(npmrcConfig: 'my-custom-nprc') {

          sh 'npm test'
        }
        }
      }
  }
}