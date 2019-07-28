pipeline {
  agent any
  stages {
    stage('1') {
      parallel {
        stage('1') {
          steps {
            sh 'echo 1'
          }
        }
        stage('1.1') {
          steps {
            sh 'echo 1.1'
          }
        }
        stage('1.2') {
          steps {
            sh 'echo 1.2'
          }
        }
      }
    }
    stage('2') {
      steps {
        sh 'echo 2'
      }
    }
    stage('3') {
      steps {
        sh 'echo 3'
      }
    }
  }
}