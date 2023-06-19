pipeline {
 agent any
 stages { 
   stage ('BUILD') {
     steps {
       echo "this is build stage"
      sh 'sleep 5'
     }
   }
 stage ('TEST PARELLEL') {
  parallel {
  stage ('TEST ON CHROME') {
   steps {
    echo "this is test on chrome browser"
      sh 'sleep 5; exit 1'
     }
   }
  }
 }
  stage ('TEST ON SAFARI') {
   steps {
    echo "this is test on safari browser"
      sh 'sleep 5; exit 1'
     }
   }
  stage ('DEPLOY') {
   parallel {
   stage ('SERVER1') {
     steps {
       echo "this is deploy to server 1"   
      sh 'sleep 5'
     }
   }
   }
    stage ('SERVER2') {
     steps {
       echo "this is deploy to server 2"   
      sh 'sleep 5'
     }
   }
    stage ('SERVER3') {
     steps {
       echo "this is deploy to server 3"   
      sh 'sleep 5'
     }
   }
 }
}
}
