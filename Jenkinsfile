pipeline {
    agent any

    stages {
        stage('clonar repositorio') {
            steps {
               git branch: 'main', url: 'https://github.com/oqvine/jenkinsfile-api-rest'
            }
        }
        stage('Instalar dependencias') {
            steps {
               bat 'npm install'
            }
        }
        stage('Excecutar testes') {
            steps {
               bat 'npm run cy:run'
            }
        }
    }
}
