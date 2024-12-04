pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                powershell 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                powershell 'npm run build'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                powershell 'npm test'
            }
        }
    }
}
