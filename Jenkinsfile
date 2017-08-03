pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh 'mvn -version'
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}