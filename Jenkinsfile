pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/maguilaes/jenkins-compose.git'
            }
        }
    }
}
