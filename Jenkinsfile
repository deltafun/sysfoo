pipeline {
  agent any
  stages{
      stage("sysfoo"){
          steps{
              echo 'compile maven app'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'test maven app'
              sh 'mvn clean test'
          }
      }
      stage("package"){
          steps{
              echo 'package maven app'
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