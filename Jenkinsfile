pipeline {
  agent any
  triggers { 
    pollSCM('* * * * *') 
  }
  stages {
    stage('build') {
      steps {
        sh 'echo \'build\''
        echo "Deploying ${params.RELEASE_VERSION} in ${env.ENV_STACK}"
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
  environment {
    ENV_STACK = 'staging'
  }
  parameters {
    string(name: 'RELEASE_VERSION', defaultValue: '1.0.0', description: 'Application git release tag version')
  }
}
