pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Run Python') {
            steps {
                dir('python-service') {
                    sh 'python3 app.py'
                }
            }
        }
    }
}
