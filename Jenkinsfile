#!/usr/bin/env groovy
pipeline {
  agent any
  stages {

    stage('test') {
      steps {
        sh "docker container run --rm -w"
      }
    }

    stage('package') {
      steps {
        sh "chmod +x ./scripts/build.sh"
        sh "./scripts/build.sh"
      }
    }

    stage('deploy') {
      steps {
        sh "chmod +x ./scripts/deploy.sh"
        sh "./scripts/deploy.sh"
      }
    }

  }
}
