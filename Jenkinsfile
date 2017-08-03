pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-v /Users/vfedasenka/.m2'
    }
    
  }
  stages {
    stage('Init') {
      steps {
        sh 'mvn install'
      }
    }
  }
}