pipeline {
  agent {
      label 'maven'
  }
  stages {
    stage('Build') {
      steps {
        dir 'quarkus-quickstart'
        sh "./mvnw clean package -Dquarkus.container-image.build=true"
      }
    }
  }
}