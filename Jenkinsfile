#!groovy

pipeline {
    agent any 
    stages {
        stage('test') { 
            steps {
                sh 'uptime'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}

