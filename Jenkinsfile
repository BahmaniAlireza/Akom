pipeline {
  agent any
  stages {
    stage('Stage1') {
      parallel {
        stage('Stage1') {
          steps {
            sh 'echo "Stage1 ..."'
          }
        }
        stage('Stage5') {
          steps {
            sh 'echo "Stage5"'
          }
        }
        stage('Stage7') {
          steps {
            sh 'echo "Stage7"'
          }
        }
      }
    }
    stage('Stage2') {
      parallel {
        stage('Stage2') {
          steps {
            sh 'echo "Stage2"'
          }
        }
        stage('Stage6') {
          steps {
            sh 'echo "Stage6"'
          }
        }
      }
    }
    stage('Stage3') {
      steps {
        sh 'echo "Stage3"'
      }
    }
    stage('Stage4') {
      steps {
        sh 'echo "Stage4"'
      }
    }
  }
}