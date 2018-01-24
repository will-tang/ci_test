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
            sh 'ssh -o StrictHostKeyChecking=no -l ci-test.eastus.cloudapp.azure.com mkdir -p /opt/test_pipe'
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