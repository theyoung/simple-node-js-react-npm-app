pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3001:3000'
        }
    }
    environment {
        CI = 'true' 
        HOME = '.'
    }
    stages {
        stage('Build') {
            steps {
                sh 'hostname'
                sh 'npm install'
            }
        }
        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }
    }
}
