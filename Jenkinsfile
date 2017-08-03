pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'sudo mvn -version'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}