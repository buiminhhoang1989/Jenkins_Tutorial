pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat 'ant main'
          }
        }
        stage('Test') {
          steps {
            junit 'testReport/*.xml'
            mail(subject: '[Jenkins] Reprot status', body: 'a', from: 'hoangbm@lifull-tech.vn', to: 'hoangbm@lifull-tech.vn')
          }
        }
      }
    }
  }
}