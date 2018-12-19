pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package -Dmaven.test.skip=true'
        archiveArtifacts 'target/*.jar'
      }
    }
    stage('Deploy to DIT') {
      steps {
        echo 'Deploying to DIT'
      }
    }
    stage('Deploying to SIT') {
      steps {
        echo 'Deploying to SIT'
      }
    }
    stage('Approval') {
      steps {
        input(message: 'Approve for PreProd', submitter: 'mohan')
      }
    }
    stage('Deploy To Preprod') {
      steps {
        echo 'Deploying to preprod'
      }
    }
  }
}