pipeline {
    agent { label 'docker-agent' }
    environment {
        DOCKER_IMAGE_NAME = 'maguilaes/jenkins-compose'
    }
    agent{label 'docker-agent'}
    pipeline {
    agent any

    environment {
        DOCKER_IMAGE_NAME = "maguilaes/simple-nodejs"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: '${env.BRANCH_NAME}', url: 'https://github.com/maguilaes/jenkins-compose.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                   sh "docker build -t ${DOCKER_IMAGE_NAME}:${env.BUILD_NUMBER} ."
                }
            }
        }
}
