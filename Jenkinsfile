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
                sh 'echo login: ${USERNAME_USR} pass: ${PASSWORD_PSW}'
                sh 'uptime'
            }
        }
    }
}
