pipeline {
  agent any
  stages {
    stage('1') {
      parallel {
        stage('checkout') {
          steps {
            sh 'echo 1'
            git(url: 'https://github.com/iluwatar/java-design-patterns.git/', branch: 'master', changelog: true)
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
    stage('uitest') {
      steps {
        sh 'echo uitest'
      }
    }
  }
}