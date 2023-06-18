pipeline {
 agent none
 stages { 
   stage ('BUILD') {
    agent any
     steps {
       echo "this is build stage"
      sh 'sleep 5'
     }
   }
 
 stage ('TEST') {
  agent { label 'jenkins'}
     steps {
       echo "this is build stage" 
      sh 'sleep 5'
     }
   }

  stage ('DEPLOY') {
   agent { label 'jenkins'}
     steps {
       echo "this is build stage"   
      sh 'sleep 5'
     }
   }
 }
}
