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
    stage('npm install') {
      steps {
        sh 'npm install'
      }
    }
    stage('Run Tests') {
      steps {
        sh 'JUNIT_REPORT_PATH=./test-results.xml ./node_modules/mocha/bin/mocha --reporter mocha-jenkins-reporter'
      }
    }
    stage('Capture Test Results') {
      steps {
        junit 'test-results.xml'
      }
    }
  }
}