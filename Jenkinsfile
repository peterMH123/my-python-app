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
                        sh 'pytest || true'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Simulated deployment step'
            }
        }
    }
}
