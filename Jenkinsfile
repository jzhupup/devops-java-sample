pipeline {
  agent any
  stages {
    stage('stage3') {
      steps {
        echo '3'
      }
    }

    stage('stage4') {
      parallel {
        stage('stage4') {
          steps {
            echo '4'
            echo '4.1'
          }
        }

        stage('stage5') {
          steps {
            echo '5'
          }
        }

      }
    }

  }
}