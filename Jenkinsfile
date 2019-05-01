pipeline {
  agent any
  stages {
    stage('Check for file-1.txt') {
      steps {
        sh 'cat file-1.txt'
      }
    }
    stage('Check for file-2.txt') {
      steps {
        sh 'cat file-2.txt'
      }
    }
  }
}