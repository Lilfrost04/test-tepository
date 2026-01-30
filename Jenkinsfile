pipeline {
    agent {
        dockerfile true
    }
    triggers { pollSCM('* * * * *') }
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
