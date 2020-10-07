#!/usr/bin/env groovy

pipeline {
  agent {
      label 'maven'
  }
  stages {
    stage('Checkout') {
        steps {
            sh 'git clone https://github.com/jeichler/quarkus-quickstart.git'
        }
    }
    stage('Build') {
      steps {
        sh "cd ${WORKSPACE}/quarkus-quickstart && ./mvnw clean package -Popenshift"
      }
    }
    stage('Test') {
      steps {
        echo 'have some meaningful tests'
      }
    }
    stage('Your next step') {
      steps {
        echo 'usually we do a bit more in pipelines, right?'
      }
    }
  }
}