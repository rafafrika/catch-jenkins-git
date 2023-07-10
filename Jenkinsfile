pipeline {
    agent any
    
    stages {
        stage('Clone Repositório') {
            steps {
                // Clonar o repositório contendo o Jenkinsfile
                git branch: 'main', url: 'https://github.com/rafafrika/verademo-dotnet.git'
            }
        }
        
        stage('Carregar e Executar Jenkinsfile') {
            steps {
                // Carregar e executar o Jenkinsfile do repositório clonado
                load 'verademo-dotnet/Jenkinsfile'
            }
        }
    }
}