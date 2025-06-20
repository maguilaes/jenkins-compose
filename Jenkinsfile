pipeline {
    agent{label 'docker-agent'}
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: '${env.BRANCH_NAME}', url: 'https://github.com/maguilaes/jenkins-compose.git'
            }
        }
    }
}
