pipeline {
  agent any
  stages {
    stage("run frontend") {
      steps {
        echo 'exucting yarn...'
        nodejs('Node-20.8') {
          sh 'yarn install'
        }
      }
    }
Please wait while Jenkins is getting ready to work ...

    stage('run backend') {
      steps {
        echo 'executing gradel...'
        wihGradle() {
          sh './gradlew -v'
        }
      }
    }
  }
    
        
}
