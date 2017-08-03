pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'echo $USER'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}