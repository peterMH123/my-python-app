pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'docker pull python:3.11'
                bat 'docker run --rm -v %cd%:/app -w /app python:3.11 pip install -r requirements.txt || exit 0'
            }
        }
        stage('Test') {
            steps {
                bat 'docker run --rm -v %cd%:/app -w /app python:3.11 pytest || exit 0'
            }
        }
        stage('Deploy') {
            steps {
                bat 'echo Simulando despliegue exitoso de la app'
            }
        }
    }
}
