pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                bat 'git checkout main'
            }
        }
        stage('Build') {
            steps {
                bat '.\\build.bat'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
    }
}
