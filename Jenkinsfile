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
          sshagent (credentials: ['azureuser']) {
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