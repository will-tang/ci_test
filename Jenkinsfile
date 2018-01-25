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
            sh 'hostname -i'
          }
        }
      }
    }
    stage('Test') {
      steps {
        script {
          sshagent (['41bcee21-1f60-4df7-b4c6-2fb94c2a6606']) {
            sh 'ssh azureuser@ci-test.eastus.cloudapp.azure.com "uname -a"'
          }
        }
        
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}