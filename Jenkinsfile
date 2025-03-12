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
                bat 'docker build -t mi-pagina-web .'
            }
        }
        stage('Deploy') {
            steps {
                bat 'docker stop mi-contenedor || true'
                bat 'docker rm mi-contenedor || true'
                bat 'docker run -d -p 8080:80 --name mi-contenedor mi-pagina-web'
            }
        }
    }
}
