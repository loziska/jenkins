bat 'chcp 65001'

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/loziska/jenkins.git', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}