pipeline {
    agent{label 'docker-agent'}
    pipeline {
    agent any

    environment {
        DOCKER_IMAGE_NAME = "maguilaes/simple-nodejs"
//        DEPLOY_SERVER = "192.168.0.107"
  //      DEPLOY_USER = "maae"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: '${env.BRANCH_NAME}', url: 'https://github.com/maguilaes/simple-nodejs.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh " docker build -t ${DOCKER_IMAGE_NAME}:${env.BUILD_NUMBER} ."
                }
            }
        }    
    }
}
