pipeline{
    stages {
        stage('install'){
            steps{
                sh 'apt-get install python'
                sh 'pip install bandit, flake8'
            }
        }
        stage('Python Bandit Security Scan'){
            steps{
                sh 'bandit *.py'
            }
        }
        stage('Python flake8 Security Scan'){
            steps{
                sh 'flake8 *.py'
            }
        }
        stage ('run'){
            steps {
                sh 'python test.py'
            }
        }
    }
}
