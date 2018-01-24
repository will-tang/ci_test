pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build'
          }
        }
        stage('Verify Tools') {
          steps {
            sh 'python --version'
          }
        }
        stage('Get Hostname') {
          steps {
            sh 'uname -a'
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Test'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}