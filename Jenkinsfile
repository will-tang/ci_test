pipeline {
  agent any
  
  parameters {
        string(
          name: 'RELEASE_VERSION', 
          defaultValue: '1.0.0', 
          description: 'Application git release tag version')
  }
  
  environment { 
        ENV_STACK = 'staging'
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
}
