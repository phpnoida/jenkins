pipeline {
  agent {
    docker {
      image 'node:16-alpine' 
       args '-v /var/run/docker.sock:/var/run/docker.sock' // Allow Docker commands inside the container
    }
  }
  stages {
    stage('Test') {
      steps {
        sh 'node --version'
        sh 'docker --version'
      }
    }
  }
}
