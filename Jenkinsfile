pipeline {
 agent none
 stages { 
        stage ('Webhook') {
         agent { label 'master'}
            steps {
                script {
                    def payload = httpRequest authentication: 'webhook', url: 'http://43.204.140.74:8080/job/pipeline/1/console'
                    // Process the payload and trigger subsequent pipeline steps as needed
                }
            }
        }
   stage ('BUILD') {
    agent { label 'master'}
     steps {
       echo "this is build stage"
      sh 'sleep 5'
     }
   }
 stage ('TEST PARELLEL') {
  parallel {
  stage ('TEST ON CHROME') {
   agent { label 'master'}
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
   parallel {
    stage ('DEPLOY ON SERVER 1') {
   agent { label 'masters'}
 steps {
  echo " this is server1 deploy "
  sh 'sleep 5'
 }
  }
      stage ('DEPLOY ON SERVER 2') {
   agent { label 'jenkins'}
 steps {
  echo " this is server2 deploy "
  sh 'sleep 5'
 }
}
 }
}
 }
}
