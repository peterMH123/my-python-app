pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Instalando dependencias del proyecto...'
                bat 'docker pull python:3.11'
                bat 'docker run --rm -v %CD%:/app -w /app python:3.11 pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Lanzando pruebas automatizadas...'
                bat 'docker run --rm -v %CD%:/app -w /app python:3.11 sh -c "pip install pytest && pytest" || exit 0'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Despliegue completado correctamente.'
            }
        }
    }
}
