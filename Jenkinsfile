pipeline {
    agent {
        dockerfile true
    }
    environment { 
        CC = 'clang'
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo ${JOB_NAME}'
            }
        }
    }
}
