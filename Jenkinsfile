pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'echo \'build\''
      }
    }
    stage('test') {
      steps {
        sh 'echo \'test by trigger\''
      }
    }
    stage('deploy') {
      steps {
        sh 'echo \'WE ARE DEPLOYING\''
      }
    }
  }
}