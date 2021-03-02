pipeline {
  agent any
  stages {
    stage('checkout project') {
      steps {
        checkout scm
      }
    }

    stage('stop node docker') {
      steps {
        sh 'docker rm -f node-docker-sample_server_1 | true'
      }
    }

    stage('start docker node') {
      steps {
        sh 'docker-compose up -d server'
      }
    }

  }
}