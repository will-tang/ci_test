pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                // checkout scm

                // sh "composer install"
                // sh "cp .env.example .env"
                // sh "php artisan key:generate"
                sh "echo 'build'"
            }
        }

        stage('test') {
            steps {
                // sh "./vendor/bin/phpunit"
                // properties([pipelineTriggers([[$class: 'GitHubPushTrigger'], pollSCM('* * * * *')])])
                // checkout scm
                // env.PATH = "${tool 'Maven 3'}/bin:${env.PATH}"
                // sh 'mvn clean package'
                sh "echo 'test by trigger'"
            }
        }

        stage('deploy') {
            steps {
                // ansible-playbook -i ./ansible/hosts ./ansible/deploy.yml
                sh "echo 'WE ARE DEPLOYING'"
            }
        }
    }

}
