pipeline {
  agent {
    docker {
      image 'maven:3.3.9-jdk-8'
      args '-v /Users/vfedasenka/.m2'
    }
    
  }
  stages {
    stage('Build stage') {
      steps {
        sh 'mvn install'
      }
    }
    stage('Report') {
      steps {
        junit(testResults: 'target/surefire-reports/**/*.xml', allowEmptyResults: true)
        archiveArtifacts 'target/*.jar'
      }
    }
  }
}