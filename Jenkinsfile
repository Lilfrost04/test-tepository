#!groovy

pipeline {
    agent {
        docker { image 'node:24.13.0-alpine3.23' }
    }
    stages {
        stage('test') { 
            steps {
                sh 'node --eval "console.log(process.platform,process.env.CI)"'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}

