pipeline {
    agent any

    stages {
        stage('Declarative: Checkout SCM') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                echo 'Installing dependencies...'
                powershell '''
                    npm install --save-dev webpack-cli
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
                powershell '''
                    npm run build
                '''
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
    }
}
