pipeline {
  agent {
    docker {
      image 'docker'
      args '-v /var/run/docker.sock:/var/run/docker.soc'
    }

  }
  stages {
    stage('stage1') {
      steps {
        echo 'STAGEAAAAA'
      }
    }
  }
}