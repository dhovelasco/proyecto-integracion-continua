pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                checkout scm
            }
        }

        stage('Limpiar Entorno Viejo') {
            steps {
                bat 'docker-compose down --remove-orphans'
            }
        }

        stage('Desplegar Infraestructura') {
            steps {
                bat 'docker-compose up -d'
            }
        }
    }
}
