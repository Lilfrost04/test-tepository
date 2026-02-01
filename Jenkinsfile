pipeline {
    agent {
        any
    }
    triggers { pollSCM('* * * * *') }
    stages {
        stage('docker login') {
            checkout scm

            docker.withRegistry('https://hub.docker.com', 'docker_hub_creds') {
                def customImage = docker.build("lilfrost20:${env.BUILD_ID}")
                customImage.push()
            }
        }

        
        // stage('docker login') {
        //     steps {
        //         withCredentials([usernamePassword(credentialsId: 'docker_hub_creds', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]) {
        //         sh 'docker login -u $USERNAME -p $PASSWORD'
        //         }
        //     }
        // }
        // stage('build docker image') {
        //     steps {
        //         sh 'docker build -t lilfrost20/testapp:latest .'
        //     }
        // }
        // stage('push docker image') {
        //     steps {
        //         sh 'docker push lilfrost20/testapp:latest .'
        //     }
        // }
    }
}
