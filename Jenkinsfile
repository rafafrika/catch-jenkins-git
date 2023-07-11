pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Clonar o segundo repositório
                echo 'Hello World!'
                git branch: 'main', credentialsId: 'github-ssh', url: 'git@github.com:rafafrika/verademo-dotnet.git'
            }
        }
        
        stage('Execute Pipeline do Segundo Jenkinsfile') {
            steps {
                echo 'Hello World! 2'
                dir('verademo-dotnet') {
                    // Executar o Jenkinsfile do segundo repositório
                    script {
                        def secondJenkinsfile = load './Jenkinsfile'
                        secondJenkinsfile.execute()
                    }
                }
                echo 'Hello World! 3'
            }
        }
        
        // Adicione aqui as outras etapas da sua pipeline
        stage('Build') {
            steps {
                echo 'Hello World! 4'
            }
        }
    }
}