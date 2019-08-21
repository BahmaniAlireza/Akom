def label = "worker-${UUID.randomUUID().toString()}"

podTemplate(label: label, containers: [
  containerTemplate(name: 'docker', image: 'docker', command: 'cat', ttyEnabled: true)
],
volumes: [
  hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock')
]) {
  node(label) {
     stage('Test') {
        container('docker') {
          sh """
            echo "test" 
            """
        }
    }
    stage('Build') {
      container('docker') {
        sh "echo build stage"
      }
    }
}
