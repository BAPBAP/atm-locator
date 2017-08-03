pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'id -un'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}