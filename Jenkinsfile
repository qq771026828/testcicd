pipeline {
  agent any
  stages {
    stage('1') {
      parallel {
        stage('checkout') {
          steps {
            sh 'echo 1'
            git(url: 'https://github.com/iluwatar/java-design-patterns.git/', branch: 'master', changelog: true, credentialsId: '6ffcb27e0b0f43e727d3f02c4328b00095f54d62')
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
    stage('test') {
      parallel {
        stage('sonartest') {
          steps {
            sh 'echo sonartest'
          }
        }
        stage('findbugs') {
          steps {
            sh 'echo findbugs'
          }
        }
        stage('robotest') {
          steps {
            sh 'echo robottest'
          }
        }
        stage('uinttest') {
          steps {
            sh 'echo unittest'
          }
        }
      }
    }
    stage('deploy') {
      steps {
        sh 'echo delpoy'
      }
    }
  }
}