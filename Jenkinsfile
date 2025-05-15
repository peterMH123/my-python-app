pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                bat 'docker pull python:3.11'
                bat 'docker run --rm python:3.11 python --version'
            }
        }
    }
}
