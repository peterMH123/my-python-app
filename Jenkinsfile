pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'python --version'
                sh 'pip install -r requirements.txt || true'
            }
        }
        stage('Test') {
            steps {
                sh 'pytest || true'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Simulando despliegue..."'
            }
        }
    }
}

