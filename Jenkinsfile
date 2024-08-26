pipeline{
  agent any
  stages{
    stage('checkout'){
      steps{
        echo 'checkout'
      }
    }
    stage ('test'){
      steps{
        bat 'mvn test'
      }
    }
    stage('package'){
      steps{
      bat 'mvn package'
    }
    }
    stage('consolidate result'){
      steps{
      input ('Do you want to continue')
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts 'target/*.jar'
      }
    }
  }
}
