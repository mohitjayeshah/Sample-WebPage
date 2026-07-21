pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://gitlab.com/username/DemoApp.git'
            }
        }

        stage('Build') {
            steps {
                // Replace with 'sh "echo Building..."' if Maven isn't installed on Jenkins host
                sh 'mvn clean compile' 
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Application Deployed Successfully!'
            }
        }
    }
}
