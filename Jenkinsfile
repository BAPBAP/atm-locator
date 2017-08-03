pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'sudo docker'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}