pipeline{
    agent { any {image 'python:3.12.1-alpine3.19' } }
    stages {
        stage('build'){
            steps{
                sh 'python --version'
            }
        }
        stage ('run'){
            steps {
                sh 'python test.py'
            }
        }
    }
}
