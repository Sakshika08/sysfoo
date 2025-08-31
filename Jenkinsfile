pipeline {
  agent any

  tools {
     maven 'Maven 3.9.6'  
  }
  stages{
      stage("build"){
          steps{
              echo 'compiling the app'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'Running unit test'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'Generating artifacts'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
