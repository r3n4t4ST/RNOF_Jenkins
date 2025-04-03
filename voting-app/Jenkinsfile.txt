pipeline {
    agent { label 'docker-agent' } 
    stages {
        stage('Imprimir Mensaje') {
            steps {
                echo '¡Soy RNOF y estoy usando Pipeline ejecutándose en el agente Docker!'
            }
        }
        stage('Ejecutar Script en el Agente') {
            steps {
                sh 'echo "Este es un script ejecutado desde el agente" > output.txt'
            }
        }
    }
}
