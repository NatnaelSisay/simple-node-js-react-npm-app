pipeline{
  agent any
  stages{
    stage("Buid"){
      steps{
        sh "npm install"
      }
    }

    stage("Test"){
      steps {
        sh "./jenkins/scripts/test.sh"
      }
    }

    stage("Deliver") {
      steps {
        sh "./jenkins/scripts/deliver.sh"
        input message: "Click proccede"
        sh "./jenkins/scripts/kill.sh"
      }
    }
  }
}