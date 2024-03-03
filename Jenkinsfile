pipeline {
  agent any
  stages {
      stage('Install dependencies') {
         steps {
          withNPM(npmrcConfig: 'd13fbbfd-bd46-49ab-bf86-08ac26acf679') {
            sh 'npm ci'
          }
        }
      }
      stage('Run tests'){
        steps {
        withNPM(npmrcConfig: 'd13fbbfd-bd46-49ab-bf86-08ac26acf679') {

          sh 'npm test'
        }
        }
      }
  }
}