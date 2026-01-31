pipeline {
    agent {
        dockerfile true
    }
    triggers { pollSCM('* * * * *') }
    stages {
        stage('docker login') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'docker_hub_creds', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]) {
                sh 'docker login --username ${USERNAME} --password ${PASSWORD}'
                }
            }
        }
        stage('build docker image') {
            steps {
                sh 'docker build -t lilfrost20/testapp:latest .'
            }
        }
        stage('push docker image') {
            steps {
                sh 'docker push lilfrost20/testapp:latest .'
            }
        }
    }
}
