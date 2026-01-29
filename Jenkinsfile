pipeline {
    agent {
        dockerfile true
    }
    environment {
        USERNAME = credentials('my_credentials')
        PASSWORD = credentials('my_credentials')
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo login: ${USERNAME} pass: ${PASSWORD}'
            }
        }
    }
}
