pipeline {
  
  agent any 
  parameters {
    choice(name: 'VERSION', choice: ['1.1.0','1.2.0', '1.3.0'], description: '')
    booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }
  
  environments {
    NEW_VERSION = '1.3.0'
    SERVER_CREDENTIALS = credentials('server-credentials')
   
  }
  
  stages {

    stage("build"){

      steps{
        echo ' building the application'
        echo 'Scan periodically after every minute'
        echo "building version ${NEW_VERSION}"
      }
    }

    stage("test"){
      when {
        expression {
          params.executeTest
        }
      steps{
        echo ' testing the applirequestscation'
      }
    }


    stage("deploy"){

      steps{
        echo ' deploying the application'
        echo "deployin version ${params.VERSION}" 
        echo "Deploying with ${SERVER_CREDENTIALS}"
        sh "${SERVER_CREDENTIALS}"
      }
    }
  }
}
