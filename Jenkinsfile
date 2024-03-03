pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
          withNPM(npmrcConfig: 'bfde068f-3bff-4c4b-a7c4-8343cbcd6f65') {
            bat 'npm ci'
          }
        }
      }
      stage('Run tests'){
        steps {
        withNPM(npmrcConfig: 'bfde068f-3bff-4c4b-a7c4-8343cbcd6f65') {

          bat 'npm test'
        }
        }
      }
  }
}