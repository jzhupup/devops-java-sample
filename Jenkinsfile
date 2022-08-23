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
    stage('阶段 3-1') {
      steps {
        useCustomStepPlugin(key: 'SYSTEM:artifact_docker_push', version: 'latest', params: [properties:'[]',image:'贾增辉',repo:'jzh-test',project:'quangongnengdevopspingtai',username:'${PROJECT_TOKEN_GK}',password:'${PROJECT_TOKEN}'])
      }
    }
  }
}