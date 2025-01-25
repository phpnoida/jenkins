pipeline {
    agent any
    stages {
        stage('Test Node.js API') {
            steps {
                script {
                    echo 'testing api....'
                    echo 'added to check automation hingi...'
                }
            }
        }
        stage('Git Configuration') {
            steps {
                script {
                    echo 'configuring git...'
                }
            }
        }
        stage('Docker Login') {
                        when 
                            {
                                expression {
                                    BRANCH_NAME == 'dev'
                                }
                            }
               
            

            steps {
                script {
                    echo 'docker login..'
                }
            }
        }
        stage('AWS ECR Login') {
             when {
                branch 'main'
            }
            steps {
                script {
                   echo 'aws login..'
                }
            }
        }
        stage('Push Image to ECR') {
             when {
                branch 'main'
            }
            steps {
                script {
                    echo 'push image to dockerhub..'
                }
            }
        }
        stage('Deploy to EC2') {
             when {
                branch 'main'
            }
            steps {
                script {
                   echo 'deploying to server..'
                }
            }
        }
    }
}
