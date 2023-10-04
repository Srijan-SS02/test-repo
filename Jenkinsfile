pipeline {
  
  agent any 
  environments {
    NEW_VERSION = '1.3.0'
    SERVER_CREDENTIALS = credentials('server-credentials')
   
  }
  stages {

    stage("build"){

      steps{
        echo ' building the application'
        echo 'Scan periodically after every minute'
        echo "building version ${NEW_VERSION}
      }
    }

    stage("test"){

      steps{
        echo ' testing the application'
      
      }
    }


    stage("deploy"){

      steps{
        echo ' deploying the application'
        echo "Deploying with ${SERVER_CREDENTIALS}"
        sh "${SERVER_CREDENTIALS"}
      }
    }
  }
}
