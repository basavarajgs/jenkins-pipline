pipeline {
 agent none
 stages { 
   stage ('BUILD') {
    agent { label 'jenkins'}
     steps {
       echo "this is build stage"
      sh 'sleep 5'
     }
   }
 stage ('TEST PARELLEL') {
  parallel {
  stage ('TEST ON CHROME') {
   agent { label 'jenkins'}
   steps {
    echo "this is test on chrome browser"
      sh 'sleep 5'
     }
   }
  stage ('TEST ON SAFARI') {
   agent { label 'jenkins'}
   steps {
    echo "this is test on safari browser"
      sh 'sleep 5'
     }
   }
  }
 }
  stage ('DEPLOY') {
   agent { label 'jenkins'}
 steps {
  echo " this is deploy stage "
  sh 'sleep 5'
 }
  }
 }
}
