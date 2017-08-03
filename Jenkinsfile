pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'docker'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}