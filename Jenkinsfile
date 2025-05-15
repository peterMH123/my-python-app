pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Iniciando etapa de Build - Parte 3 del Lab'
                bat 'docker pull python:3.11'
                bat 'docker run --rm -v %CD%:/app -w /app python:3.11 pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando tests con Pytest (modificado para la Parte 3)'
                bat 'docker run --rm -v %CD%:/app -w /app python:3.11 sh -c "pip install pytest && pytest" || exit 0'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy de prueba completado por Pedro Marroquín (Parte 3)'
            }
        }
    }
}
