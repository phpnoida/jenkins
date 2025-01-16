pipeline {
    agent {
        docker {
            image 'docker-custom-img:latest'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
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
