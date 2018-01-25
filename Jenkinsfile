#!/usr/bin/env groovy

node('master') {
    try {
        stage('build') {
            // checkout scm

            // sh "composer install"
            // sh "cp .env.example .env"
            // sh "php artisan key:generate"
            sh "echo 'build'"
        }

        stage('test') {
            // sh "./vendor/bin/phpunit"
          properties([pipelineTriggers([[$class: 'GitHubPushTrigger'], pollSCM('H/15 * * * *')])])
          // checkout scm
          // env.PATH = "${tool 'Maven 3'}/bin:${env.PATH}"
          // sh 'mvn clean package'
          sh "echo 'test by trigger'"
        }

        stage('deploy') {
            // ansible-playbook -i ./ansible/hosts ./ansible/deploy.yml
            sh "echo 'WE ARE DEPLOYING'"
        }
    } catch(error) {
        throw error
    } finally {

    }

}
