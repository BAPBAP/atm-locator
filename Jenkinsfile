pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh '''echo $USER
docker'''
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}