pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh './gradlew clean build'
            }
        }
        stage('Fake Upload to Artifactory') {
            steps {
                echo 'Simulating upload of build/libs/demo-microservice-1.0.0.jar to Artifactory...'
            }
        }
        stage('Run DemoService') {
            steps {
                sh 'java -cp build/classes/java/main DemoService'
            }
        }
    }
}
