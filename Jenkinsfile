pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        sh '''cd /
find . | grep docker'''
      }
    }
  }
}