pipeline{
  agent any
  stages{
    stage("parallel execution"){
      steps{
    parallel(
      a:{
      bat 'mvn install'
      }
      b:{
      bat 'mvn clean'
      }
      c:{
        bat 'mvn package'
      }
      )
      }
    }
  }
}
