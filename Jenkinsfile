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
                echo 'Building application...'
                sh 'python3 -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest'
            }
        }

        stage('Validation') {
            steps {
                echo 'Validating application...'
                sh 'python3 app.py'
            }
        }
    }
}
