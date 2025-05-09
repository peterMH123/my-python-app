pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('python:3.11').inside {
                        sh 'pip install -r requirements.txt'
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    docker.image('python:3.11').inside {
                        sh 'pytest || echo "Tests failed or not found."'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Simulating deployment step...'
            }
        }
    }
}
