pipeline {
  agent any
  stages {
    stage('BUILD') {
      steps {
        echo "This is the build stage"
        sh 'sleep 5'
      }
    }
    stage('TEST AND DEPLOY') {
      parallel {
        stage('TEST') {
          stages {
            stage('TEST ON CHROME') {
              steps {
                echo "This is the test on chrome browser"
                sh 'sleep 5; exit 1'
              }
            }
            stage('TEST ON SAFARI') {
              steps {
                echo "This is the test on safari browser"
                sh 'sleep 5; exit 1'
              }
            }
          }
        }
        stage('DEPLOY') {
          stages {
            stage('SERVER1') {
              steps {
                echo "This is the deploy to server 1"
                sh 'sleep 5'
              }
            }
            stage('SERVER2') {
              steps {
                echo "This is the deploy to server 2"
                sh 'sleep 5'
              }
            }
            stage('SERVER3') {
              steps {
                echo "This is the deploy to server 3"
                sh 'sleep 5'
              }
            }
          }
        }
      }
    }
  }
}
