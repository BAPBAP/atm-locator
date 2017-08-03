pipeline {
  agent any
  stages {
    stage('Init') {
      steps {
        parallel(
          "Init": {
            sh '''PATH=$PATH:/Users/vfedasenka/dev/tools/maven-mp/bin
mvn -version'''
            
          },
          "PWD": {
            sh 'pwd'
            
          }
        )
      }
    }
  }
}