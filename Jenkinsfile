pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh 'mvn clean package -Dmaven.test.skip=true'
      }
    }
  }
}