pipeline {
 agent none
 stages {
  agent any 
   stage ('BUILD') {
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
