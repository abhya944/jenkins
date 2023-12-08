pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'echo %BUILD_ID%'
      }
    }

    stage('TEST') {
      parallel {
        stage('TEST') {
          steps {
            echo 'TESTING'
            bat 'ECHO "ABHYA"'
          }
        }

        stage('TEST2') {
          steps {
            timestamps() {
              echo 'TIME'
            }

          }
        }

      }
    }

    stage('DEPLOY') {
      steps {
        readFile 'jenkins_pipeline'
      }
    }

  }
}