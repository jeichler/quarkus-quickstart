pipeline {
  agent {
      label 'maven'
  }
  stages {
    stage('Build') {
      steps {
        dir 'openshift-quickstart'
        sh "./mvnw clean package -Dquarkus.container-image.build=true"
      }
    }
  }
}