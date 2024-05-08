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
  }
}