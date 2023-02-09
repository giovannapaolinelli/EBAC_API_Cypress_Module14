pipeline {
    agent any

    stages {
        stage('Clonar o repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/giovannapaolinelli/testes-api-cy.git'
            }
        }
        stage('Instalar dependencias'){
            steps {
                bat 'npm install'
            }
        }
        stage('Iniciar servidor'){
            steps {
                bat 'npm start'
            }
        }
        stage('Executar Testes'){
            steps {
                bat 'npm run cy:run'
            }
        }
    }
}
