pipeline{
    agent { any {image 'python:3.12.1-alpine3.19' } }
    stages {
        stage('build'){
            steps{
                sh 'python --version'
                sh 'pip install bandit'
            }
        }
        stage('Python Bandit Security Scan'){
            steps{
                sh 'bandit *.py'
            }
        }
        stage ('run'){
            steps {
                sh 'python test.py'
            }
        }
    }
}
